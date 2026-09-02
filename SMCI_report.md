# SMCI

**Generated** : 2026-09-02T00:24:36.141988+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $36.71  

> 🟡 **WAIT-FOR-DIP** — spot +8.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $36.71 (+8.0% vs entrée) · entrée $33.99 · stop $31.69 · T1 $36.24 · R/R 0.98  
> ↳ P(T1 av. stop) 60 % · EV/risk 0.146 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $33.54–$34.44 (mid $33.99)
- Spot actuel : $36.71 (+8.0% au-dessus de la zone — repli à attendre)
- Stop : $31.69 (stop swing_plan-based (-13.67%))
- Targets : T1 $36.24 · R/R 0.98 | T2 $38.48 · R/R 1.95 | T3 $40.72 · R/R 2.93
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $31.69


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.67 %)** : le gap seul le franchit 0.638 % des séances (8 fois sur 1253).
   - exécution **4.557 pt plus bas** dans le cas TYPIQUE (médiane), 13.847 au p90, **15.381 au pire**
   - perte réelle **19.93 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 13.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.04 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5725** [0.4981 ; 0.6445] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4361** [0.3845 ; 0.4887] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.3682** [0.3186 ; 0.42] _(largeur 10.1 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.0 pt), swing (52.9 pt), deep (51.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.76 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.29 % contre 7.20 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5382** (β de hausse 1.2442, asymétrie 1.2363) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.949× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 32.4897 sur swing_based (1.34 ATR, 11.496 %) — p(stop avant cible) 0.378 [0.33 ; 0.43], R/R 1.558, perte reelle 17.9 % (gap inclus), CVaR 11.552 %, EV 0.1259 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 60.2 % de la queue et il ne reste que -755.68 EUR a partager. Prix du risque -0.422 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.395 %) — p(stop avant cible) 0.4751 [0.42 ; 0.53], R/R 1.706, perte reelle 16.347 % (gap inclus), EV -0.9505 % — **REFUSE**
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 18.6 % x 27.89 % + P(rien) 33.9 % x 4.82 % ne couvrent pas P(stop) 47.5 % x 16.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.34 ATR (stop 11.496 %) — p(stop avant cible) 0.378 [0.33 ; 0.43], R/R 1.558, perte reelle 17.9 % (gap inclus), EV 0.1259 % — **REFUSE**
      - refuse : R/R 1.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 2.25 ATR (stop 17.192 %) — p(stop avant cible) 0.2019 [0.16 ; 0.25], R/R 1.192, perte reelle 23.404 % (gap inclus), EV 1.5754 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.22 % > budget 12.00 %
   - 🟢 support a 3.91 ATR (stop 27.623 %) — p(stop avant cible) 0.0919 [0.06 ; 0.13], R/R 0.96, perte reelle 29.051 % (gap inclus), EV 2.3449 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.62 % > budget 12.00 %
   - 🟢 support a 4.91 ATR (stop 33.888 %) — p(stop avant cible) 0.0716 [0.05 ; 0.10], R/R 0.823, perte reelle 33.888 % (gap inclus), EV 2.0682 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.89 % > budget 12.00 %
   - 🟢 support a 5.8 ATR (stop 39.418 %) — p(stop avant cible) 0.0173 [0.01 ; 0.04], R/R 0.707, perte reelle 39.418 % (gap inclus), EV 2.217 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.42 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.566 %) — p(stop avant cible) 0.9053 [0.87 ; 0.93], R/R 6.838, perte reelle 4.078 % (gap inclus), EV -1.5992 % — **REFUSE**
      - refuse : cible atteinte seulement 6.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.84 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.905, borne haute 0.933 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 6.1 % x 27.89 % + P(rien) 3.4 % x 11.63 % ne couvrent pas P(stop) 90.5 % x 4.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.132 %) — p(stop avant cible) 0.7995 [0.75 ; 0.84], R/R 4.263, perte reelle 6.542 % (gap inclus), EV -1.2212 % — **REFUSE**
      - refuse : cible atteinte seulement 11.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.799, borne haute 0.839 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.22 %) : P(cible) 11.5 % x 27.89 % + P(rien) 8.5 % x 9.32 % ne couvrent pas P(stop) 80.0 % x 6.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.698 %) — p(stop avant cible) 0.7113 [0.66 ; 0.76], R/R 2.833, perte reelle 9.842 % (gap inclus), EV -1.9219 % — **REFUSE**
      - refuse : cible atteinte seulement 14.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.711, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.92 %) : P(cible) 14.4 % x 27.89 % + P(rien) 14.5 % x 7.38 % ne couvrent pas P(stop) 71.1 % x 9.84 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.263 %) — p(stop avant cible) 0.6281 [0.58 ; 0.68], R/R 2.239, perte reelle 12.453 % (gap inclus), EV -1.8138 % — **REFUSE**
      - refuse : p_stop_first 0.628, borne haute 0.678 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.81 %) : P(cible) 16.4 % x 27.89 % + P(rien) 20.8 % x 6.89 % ne couvrent pas P(stop) 62.8 % x 12.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.34 ATR (stop 10.269 %) — p(stop avant cible) 0.4403 [0.39 ; 0.49], R/R 1.653, perte reelle 16.875 % (gap inclus), EV -0.6473 % — **REFUSE**
      - refuse : R/R 1.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 18.7 % x 27.89 % + P(rien) 37.3 % x 4.23 % ne couvrent pas P(stop) 44.0 % x 16.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.25 ATR (stop 15.965 %) — p(stop avant cible) 0.2318 [0.19 ; 0.28], R/R 1.192, perte reelle 23.404 % (gap inclus), EV 0.8965 % — **REFUSE**
      - refuse : R/R 1.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.99 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 18.79 %) — p(stop avant cible) 0.1587 [0.12 ; 0.20], R/R 1.119, perte reelle 24.92 % (gap inclus), EV 2.0767 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.81 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.922 %) — p(stop avant cible) 0.1397 [0.11 ; 0.18], R/R 1.038, perte reelle 26.856 % (gap inclus), EV 2.0217 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.93 % > budget 12.00 %
   - 🟢 grid_snapped a 3.91 ATR (stop 26.395 %) — p(stop avant cible) 0.0961 [0.07 ; 0.13], R/R 0.998, perte reelle 27.955 % (gap inclus), EV 2.4236 % — **REFUSE**
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.40 % > budget 12.00 %
   - 🟢 grid_snapped a 4.91 ATR (stop 32.661 %) — p(stop avant cible) 0.0773 [0.05 ; 0.11], R/R 0.854, perte reelle 32.661 % (gap inclus), EV 2.1129 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.66 % > budget 12.00 %
   - 🟢 grid_snapped a 5.8 ATR (stop 38.191 %) — p(stop avant cible) 0.0396 [0.02 ; 0.06], R/R 0.73, perte reelle 38.191 % (gap inclus), EV 2.0807 % — **REFUSE**
      - refuse : R/R 0.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.19 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 40.712 %) — p(stop avant cible) 0.0136 [0.01 ; 0.03], R/R 0.685, perte reelle 40.712 % (gap inclus), EV 2.2274 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.844 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.636, perte reelle 43.844 % (gap inclus), EV 2.2423 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.84 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 46.975 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.594, perte reelle 46.975 % (gap inclus), EV 2.2335 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.98 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.107 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 0.557, perte reelle 50.107 % (gap inclus), EV 2.2306 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.11 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 36.71, ATR14 2.2993 (6.263 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 2.167 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.313 % | 36.595 | 90.43 % | 93.15 % | 94.55 % | 95.05 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.626 % | 36.4801 | 82.18 % | 87.1 % | 89.1 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.94 % | 36.3651 | 75.03 % | 81.96 % | 84.86 % | 88.07 % | 90.55 % | 93.63 % |
| 0.2 ATR | 1.253 % | 36.2501 | 67.98 % | 77.22 % | 80.42 % | 85.54 % | 89.13 % | 92.3 % |
| 0.25 ATR | 1.566 % | 36.1352 | 61.93 % | 72.68 % | 76.29 % | 82.2 % | 87.09 % | 90.55 % |
| 0.35 ATR | 2.192 % | 35.9052 | 49.45 % | 63.71 % | 69.83 % | 77.25 % | 82.72 % | 88.09 % |
| 0.5 ATR | 3.132 % | 35.5604 | 34.94 % | 50.2 % | 58.43 % | 68.76 % | 76.93 % | 83.98 % |
| 0.75 ATR | 4.698 % | 34.9855 | 17.32 % | 33.47 % | 43.09 % | 55.11 % | 66.46 % | 75.87 % |
| 1.0 ATR | 6.263 % | 34.4107 | 8.16 % | 21.98 % | 30.98 % | 43.98 % | 57.42 % | 68.99 % |
| 1.25 ATR | 7.829 % | 33.8359 | 3.93 % | 15.12 % | 22.91 % | 33.67 % | 48.68 % | 62.01 % |
| 1.5 ATR | 9.395 % | 33.2611 | 1.51 % | 9.78 % | 16.65 % | 26.59 % | 42.38 % | 55.54 % |
| 2.0 ATR | 12.527 % | 32.1114 | 0.3 % | 3.63 % | 8.58 % | 16.28 % | 30.28 % | 44.25 % |
| 2.5 ATR | 15.658 % | 30.9618 | 0.2 % | 1.61 % | 4.44 % | 10.01 % | 20.02 % | 32.24 % |
| 3.0 ATR | 18.79 % | 29.8121 | 0.2 % | 1.21 % | 2.62 % | 5.76 % | 14.43 % | 24.33 % |
| 4.0 ATR | 25.054 % | 27.5129 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.27 % |
| 6.0 ATR | 37.58 % | 22.9143 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.19 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.91 ATR | 2.43 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.98 ATR | 1.27 ATR | 1.58 ATR | 1.82 ATR | 2.50 ATR | 3.24 ATR |
| **10 s.** | 0.55 ATR | 1.21 ATR | 1.40 ATR | 1.89 ATR | 2.26 ATR | 2.50 ATR | 3.63 ATR | 4.90 ATR |
| **20 s.** | 0.78 ATR | 1.75 ATR | 1.97 ATR | 2.47 ATR | 2.96 ATR | 3.43 ATR | 4.98 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.578–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.698 %, prix 34.9854), p(touche) 33.47 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.719–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.698 %, prix 34.9854), p(touche) 43.09 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 15.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.977–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.829 %, prix 33.836), p(touche) 33.67 % (en stress 89.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.396–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.395 %, prix 33.2611), p(touche) 42.38 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.967–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (15.658 %, prix 30.9619), p(touche) 32.24 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.047 | EV/share : $0.109 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 24 % | T3 17 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 83.7 | bear 5.6 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 477.0 (= 13 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.361% → cible +2.953% / stop −1.944%, p_fill 35%, n_eff≈17.4) : P(cible|rempli) **35%** · **EV/risk +0.070** (×p_fill ; si rempli +0.38% du capital)
  - **swing** (entrée dip −7.407% → cible +6.602% / stop −6.764%, p_fill 24%, n_eff≈11.0) : P(cible|rempli) **57%** · **EV/risk +0.080** (×p_fill ; si rempli +2.24% du capital)
  - **deep** (entrée dip −11.446% → cible +9.336% / stop −10.609%, p_fill 15%, n_eff≈11.1) : P(cible|rempli) **64%** · **EV/risk +0.020** (×p_fill ; si rempli +1.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→76% · +2.0%→60% · +3.0%→45% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.2% (p90 10.79%) · excursion haute méd. +2.53% / basse méd. −2.53%
- Profil de vol intra : ouverture 4.162% vs midi 1.26% vs clôture 1.636% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. 0.037% ; recovery-V 30%
- **σ réalisé intraday** 3.955% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 67% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 37.2861 (VA 37.2146–37.3934 ; dernier close 37.28)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.26% · baisse 44% (gap-down >1% 35% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −2.79%) · haut méd +1.02% · range méd 2.28%
- Excursion ouverture 15min (n=160) : bas méd −1.19% (p90 −3.29%) · haut méd +1.48% · range méd 2.96%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.84%) · haut méd +1.58% · range méd 3.73%
- Excursion ouverture 60min (n=160) : bas méd −1.67% (p90 −4.49%) · haut méd +1.9% · range méd 4.4%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 37.28 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (120/159) · gap 41% · délai 0.0min · rebond 58% (73/120) (MFE +1.32%)
   - −1.0% : fill 30min 54% · séance 69% (111/159) · gap 35% · délai 0.0min · rebond 61% (66/111) (MFE +1.51%)
   - −1.5% : fill 30min 47% · séance 62% (100/159) · gap 22% · délai 0.1min · rebond 68% (63/100) (MFE +1.59%)
   - −2.0% : fill 30min 42% · séance 54% (87/159) · gap 16% · délai 0.7min · rebond 71% (57/87) (MFE +1.78%)
   - −3.0% : fill 30min 30% · séance 48% (75/159) · gap 10% · délai 10.5min · rebond 60% (46/75) (MFE +1.7%)
   - −4.0% : fill 30min 19% · séance 37% (56/159) · gap 6% · délai 30.0min · rebond 76% (37/56) (MFE +1.75%)
   - −5.0% : fill 30min 14% · séance 29% (46/159) · gap 4% · délai 42.5min · rebond 81% (34/46) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.83%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.98%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.83%) → stop au-delà de −1.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=903 jambes) : jambe baissière méd −1.2% (p90 −2.87%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 96% (67/69) · rebond 50% (35/67)
      · −2.0% : fill 92% (63/69) · rebond 67% (38/63)
      · −3.0% : fill 84% (57/69) · rebond 55% (33/57)
      · −4.0% : fill 67% (44/69) · rebond 76% (29/44)
      · −5.0% : fill 53% (37/69) · rebond 80% (27/37)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 40% (31/77) · rebond 75% (20/31)
      · −2.0% : fill 22% (18/77) · rebond 81% (15/18)
      · −3.0% : fill 18% (15/77) · rebond 70% (10/15)
      · −4.0% : fill 13% (10/77) · rebond 71% (6/10)
      · −5.0% : fill 12% (9/77) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 65% si les 15 1res min sont vertes (77 cas) · 23% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 17% si rouge (base 44% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **72%** · continue >prix actuel 45% ; creux résiduel méd -2.21% (q20 -3.74%) → **SL/trailing à −3.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +3.98% → **scale +2.03% / runner +3.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **17%** (continue à baisser 52%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +1.8% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.26% .. +4.68%] · haut q95 +6.04% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.54% .. +5.37%] · haut q95 +6.57% · bas q05 -5.36%
   - 2h (n=160) : retour [-4.72% .. +6.65%] · haut q95 +7.9% · bas q05 -5.86%
   - 4h (n=160) : retour [-5.22% .. +7.16%] · haut q95 +8.64% · bas q05 -6.77%
   - 6h (n=160) : retour [-5.7% .. +6.84%] · haut q95 +9.32% · bas q05 -6.91%
   - session (n=160) : retour [-6.87% .. +7.78%] · haut q95 +9.4% · bas q05 -7.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 47.2  _(neutre)_
- **ADX** : 24.7  _(pas de tendance nette)_
- **MACD** : hist -0.15  _(bearish_recent)_
- **BB** : %B 0.57 · largeur 35.7%
- **ATR** : 2.3 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.033  _(neutre)_
- **Vol ratio** : 0.49  _(volume atone)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 35.85 · MA50 31.37 · MA200 31.32  _(prix > MA20)_
- **Dist MA** : MA20 +2.4% · MA50 +17.0% · MA200 +17.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (776097 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
