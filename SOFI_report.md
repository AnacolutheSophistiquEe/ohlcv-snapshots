# SOFI

**Generated** : 2026-09-01T00:35:05.047073+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · $17.88  

> 🟡 **WAIT-FOR-DIP** — spot +5.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $17.88 (+5.8% vs entrée) · entrée $16.90 · stop $16.05 · T1 $17.52 · R/R 0.73  
> ↳ P(T1 av. stop) 71 % · EV/risk 0.074 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.130 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.78–$17.03 (mid $16.90)
- Spot actuel : $17.88 (+5.8% au-dessus de la zone — repli à attendre)
- Stop : $16.05 (stop swing_plan-based (-10.25%))
- Targets : T1 $17.52 · R/R 0.73 | T2 $18.15 · R/R 1.47 | T3 $18.77 · R/R 2.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.05


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.99 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.25 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **0.855 pt plus bas** dans le cas TYPIQUE (médiane), 0.855 au p90, **0.855 au pire**
   - perte réelle **11.105 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 10.25 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0007 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.268 % | p01 -6.52 % | pire -11.105 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1496** [0.1024 ; 0.2084] _(largeur 10.6 pt, n_eff 173.1)_
   - swing : **0.3851** [0.3349 ; 0.4372] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3776** [0.3277 ; 0.4296] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.4 observations effectives », dont la borne haute a 95 % vaut environ 18.3 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.98 %** | CVaR **-8.48 %** | vol 3.87 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 6.01 % contre 3.50 % aujourd'hui, rapport 1.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.021 ; < 1 = le √5 surestime)_
- **β de baisse : 1.827** (β de hausse 1.7089, asymétrie 1.0691) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.304× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 15.76 sur grid_snapped (2.18 ATR, 11.857 %) — p(stop avant cible) 0.2707 [0.23 ; 0.32], R/R 3.446, perte reelle 11.857 % (gap inclus), CVaR 11.857 %, EV -0.1457 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.48 ATR (stop 4.467 %) — p(stop avant cible) 0.6669 [0.62 ; 0.71], R/R 5.943, perte reelle 6.875 % (gap inclus), EV -1.5684 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.667, borne haute 0.715 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.57 %) : P(cible) 0.1 % x 40.86 % + P(rien) 33.2 % x 8.98 % ne couvrent pas P(stop) 66.7 % x 6.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 7.179 %) — p(stop avant cible) 0.4741 [0.42 ; 0.53], R/R 4.547, perte reelle 8.985 % (gap inclus), EV -0.8207 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.82 %) : P(cible) 0.1 % x 40.86 % + P(rien) 52.5 % x 6.47 % ne couvrent pas P(stop) 47.4 % x 8.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.18 ATR (stop 12.589 %) — p(stop avant cible) 0.2346 [0.19 ; 0.28], R/R 3.245, perte reelle 12.589 % (gap inclus), EV 0.103 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.59 % > budget 12.00 %
   - 🟢 support a 3.51 ATR (stop 18.946 %) — p(stop avant cible) 0.0629 [0.04 ; 0.09], R/R 2.156, perte reelle 18.946 % (gap inclus), EV 0.5042 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.95 % > budget 12.00 %
   - ⚪ grid_snapped a 0.48 ATR (stop 3.735 %) — p(stop avant cible) 0.7251 [0.68 ; 0.77], R/R 7.174, perte reelle 5.695 % (gap inclus), EV -1.5374 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.725, borne haute 0.770 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 0.1 % x 40.86 % + P(rien) 27.4 % x 9.35 % ne couvrent pas P(stop) 72.5 % x 5.70 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 5.982 %) — p(stop avant cible) 0.5547 [0.50 ; 0.61], R/R 5.216, perte reelle 7.833 % (gap inclus), EV -0.9839 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.555, borne haute 0.607 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.1 % x 40.86 % + P(rien) 44.4 % x 7.47 % ne couvrent pas P(stop) 55.5 % x 7.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 8.375 %) — p(stop avant cible) 0.4102 [0.36 ; 0.46], R/R 4.209, perte reelle 9.707 % (gap inclus), EV -0.5683 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.57 %) : P(cible) 0.1 % x 40.86 % + P(rien) 58.9 % x 5.73 % ne couvrent pas P(stop) 41.0 % x 9.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.18 ATR (stop 11.857 %) — p(stop avant cible) 0.2707 [0.23 ; 0.32], R/R 3.446, perte reelle 11.857 % (gap inclus), EV -0.1457 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.1 % x 40.86 % + P(rien) 72.8 % x 4.15 % ne couvrent pas P(stop) 27.1 % x 11.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 14.358 %) — p(stop avant cible) 0.1504 [0.12 ; 0.19], R/R 2.846, perte reelle 14.358 % (gap inclus), EV 0.3312 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.36 % > budget 12.00 %
   - 🟢 grid_snapped a 3.51 ATR (stop 18.214 %) — p(stop avant cible) 0.0664 [0.04 ; 0.10], R/R 2.243, perte reelle 18.214 % (gap inclus), EV 0.5169 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.21 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.536 %) — p(stop avant cible) 0.037 [0.02 ; 0.06], R/R 1.897, perte reelle 21.536 % (gap inclus), EV 0.4701 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.90 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.54 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 23.929 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 1.707, perte reelle 23.929 % (gap inclus), EV 0.4663 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.93 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 26.322 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.552, perte reelle 26.322 % (gap inclus), EV 0.5995 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.32 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.715 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.423, perte reelle 28.715 % (gap inclus), EV 0.6126 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.72 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 31.108 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 1.313, perte reelle 31.108 % (gap inclus), EV 0.6061 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.11 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 33.501 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.22, perte reelle 33.501 % (gap inclus), EV 0.6231 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.894 %) — p(stop avant cible) 0.0015 [0.00 ; 0.01], R/R 1.138, perte reelle 35.894 % (gap inclus), EV 0.6192 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.89 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 38.287 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.067, perte reelle 38.287 % (gap inclus), EV 0.6287 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.29 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 17.88, ATR14 0.8557 (4.786 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.376 ATR = 1.799 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.239 % | 17.8372 | 92.85 % | 95.77 % | 96.97 % | 97.37 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.479 % | 17.7944 | 85.1 % | 89.52 % | 91.93 % | 93.23 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.718 % | 17.7516 | 79.05 % | 84.98 % | 88.19 % | 90.39 % | 92.78 % | 94.76 % |
| 0.2 ATR | 0.957 % | 17.7089 | 71.6 % | 79.74 % | 83.55 % | 86.86 % | 90.45 % | 93.22 % |
| 0.25 ATR | 1.196 % | 17.6661 | 66.36 % | 75.2 % | 80.12 % | 84.13 % | 88.82 % | 91.79 % |
| 0.35 ATR | 1.675 % | 17.5805 | 52.57 % | 65.42 % | 72.15 % | 78.26 % | 85.26 % | 88.5 % |
| 0.5 ATR | 2.393 % | 17.4521 | 37.66 % | 53.33 % | 61.55 % | 68.96 % | 79.27 % | 84.29 % |
| 0.75 ATR | 3.589 % | 17.2382 | 20.24 % | 36.69 % | 46.82 % | 56.83 % | 69.72 % | 77.41 % |
| 1.0 ATR | 4.786 % | 17.0243 | 8.86 % | 24.29 % | 33.7 % | 44.89 % | 59.35 % | 68.69 % |
| 1.25 ATR | 5.982 % | 16.8104 | 4.13 % | 14.82 % | 23.51 % | 35.39 % | 50.1 % | 62.01 % |
| 1.5 ATR | 7.179 % | 16.5964 | 2.01 % | 9.38 % | 16.55 % | 27.4 % | 41.97 % | 55.44 % |
| 2.0 ATR | 9.572 % | 16.1686 | 0.7 % | 4.33 % | 8.27 % | 15.27 % | 29.17 % | 45.17 % |
| 2.5 ATR | 11.965 % | 15.7407 | 0.3 % | 1.92 % | 3.73 % | 9.4 % | 19.82 % | 35.83 % |
| 3.0 ATR | 14.358 % | 15.3129 | 0.1 % | 0.91 % | 2.83 % | 6.07 % | 14.23 % | 28.44 % |
| 4.0 ATR | 19.143 % | 14.4571 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.52 % | 14.78 % |
| 6.0 ATR | 28.715 % | 12.7457 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.20 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.82 ATR | 0.99 ATR | 1.11 ATR | 1.47 ATR | 1.93 ATR |
| **3 s.** | 0.31 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.21 ATR | 1.38 ATR | 1.90 ATR | 2.36 ATR |
| **5 s.** | 0.40 ATR | 0.89 ATR | 1.00 ATR | 1.32 ATR | 1.60 ATR | 1.80 ATR | 2.45 ATR | 3.30 ATR |
| **10 s.** | 0.61 ATR | 1.25 ATR | 1.41 ATR | 1.85 ATR | 2.22 ATR | 2.49 ATR | 3.63 ATR | 4.76 ATR |
| **20 s.** | 0.82 ATR | 1.76 ATR | 2.01 ATR | 2.69 ATR | 3.25 ATR | 3.62 ATR | 4.82 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.426–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (2.393 %, prix 17.4521), p(touche) 37.66 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.589 %, prix 17.2383), p(touche) 36.69 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 17.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.785–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.786 %, prix 17.0243), p(touche) 33.7 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.998–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.786 %, prix 17.0243), p(touche) 44.89 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.407–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.179 %, prix 16.5964), p(touche) 41.97 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.009–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (11.965 %, prix 15.7407), p(touche) 35.83 % (en stress 98.98 %)  ✅ optimum identifie (71.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.082 | EV/share : $-0.070 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 27 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 68.8 | bear 13.4 | side 17.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 143.0 (= 8 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.49% → cible +1.644% / stop −4.0%, p_fill 38%, n_eff≈16.4) : P(cible|rempli) **28%** · **EV/risk -0.052** (×p_fill ; si rempli -0.55% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→70% · +2.0%→50% · +3.0%→38% · +5.0%→12% · +8.0%→1%
- Range intraday médian 4.41% (p90 7.54%) · excursion haute méd. +2.04% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.049% vs midi 0.872% vs clôture 0.992% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑2%/↓0% ; spike-down 63% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.151 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. -0.174% ; recovery-V 23%
- **σ réalisé intraday** 2.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 18.1206 (VA 18.0481–18.7369 ; dernier close 18.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 67% · **stop −2.97%** sous le fill (sous le bruit) · cible +1.82% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 42% (gap-down >1% 21% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −1.79%) · haut méd +0.71% · range méd 1.66%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.85%) · haut méd +0.99% · range méd 2.31%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.2%) · haut méd +1.16% · range méd 2.68%
- Excursion ouverture 60min (n=160) : bas méd −1.42% (p90 −3.73%) · haut méd +1.43% · range méd 3.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 18.06 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (120/159) · gap 28% · délai 0.1min · rebond 54% (65/120) (MFE +1.26%)
   - −1.0% : fill 30min 52% · séance 65% (109/159) · gap 21% · délai 1.5min · rebond 58% (65/109) (MFE +1.19%)
   - −1.5% : fill 30min 40% · séance 60% (100/159) · gap 17% · délai 11.2min · rebond 68% (68/100) (MFE +1.47%)
   - −2.0% : fill 30min 32% · séance 46% (79/159) · gap 10% · délai 9.8min · rebond 67% (55/79) (MFE +1.82%)
   - −3.0% : fill 30min 13% · séance 34% (57/159) · gap 3% · délai 48.4min · rebond 58% (38/57) (MFE +1.13%)
   - −4.0% : fill 30min 8% · séance 17% (35/159) · gap 2% · délai 39.2min · rebond 57% (23/35) (MFE +1.36%)
   - −5.0% : fill 30min 3% · séance 9% (19/159) · gap 2% · délai 99.6min · rebond 32% (9/19) (MFE +0.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.98%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.48% (p90 −2.07%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.47% (p90 −1.45%) → stop au-delà de −1.21% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=668 jambes) : jambe baissière méd −1.08% (p90 −2.78%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 60% (40/64)
      · −2.0% : fill 84% (54/65) · rebond 74% (39/54)
      · −3.0% : fill 68% (42/65) · rebond 62% (29/42)
      · −4.0% : fill 36% (27/65) · rebond 70% (20/27)
      · −5.0% : fill 19% (15/65) · rebond 40% (8/15)
   - **flat** (22 séances) :
      · −1.0% : fill 67% (13/22) · rebond 42% (6/13)
      · −2.0% : fill 45% (8/22) · rebond 56% (5/8)
      · −3.0% : fill 35% (6/22) · rebond 38% (3/6)
      · −4.0% : fill 22% (3/22) · rebond 30% (1/3)
      · −5.0% : fill 13% (1/22) · rebond 0% (0/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (32/72) · rebond 62% (19/32)
      · −2.0% : fill 21% (17/72) · rebond 58% (11/17)
      · −3.0% : fill 11% (9/72) · rebond 60% (6/9)
      · −4.0% : fill 3% (5/72) · rebond 22% (2/5)
      · −5.0% : fill 1% (3/72) · rebond 44% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 61% si les 15 1res min sont vertes (75 cas) · 23% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **37min** → P(séance verte=clôture>ouverture) 74% si début vert vs 10% si rouge (base 41% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **74%** · continue >prix actuel 49% ; creux résiduel méd -1.54% (q20 -2.58%) → **SL/trailing à −2.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.78% / q75 +2.87% → **scale +1.78% / runner +2.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **10%** (continue à baisser 65%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.61%** (au-delà de la MAE q10 -3.61%), cible rebond +1.02% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.92% .. +3.76%] · haut q95 +4.04% · bas q05 -3.4%
   - 60min (n=160) : retour [-3.14% .. +3.78%] · haut q95 +4.56% · bas q05 -4.01%
   - 2h (n=160) : retour [-3.58% .. +3.98%] · haut q95 +5.33% · bas q05 -4.65%
   - 4h (n=160) : retour [-4.63% .. +4.61%] · haut q95 +5.68% · bas q05 -5.15%
   - 6h (n=160) : retour [-4.82% .. +4.08%] · haut q95 +5.71% · bas q05 -5.85%
   - session (n=160) : retour [-4.77% .. +5.11%] · haut q95 +5.71% · bas q05 -6.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 49.3  _(neutre)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist -0.033  _(bearish_recent)_
- **BB** : %B 0.23 · largeur 9.0%
- **ATR** : 0.86 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.13  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 68.9  _(marche en range (choppy))_
- **MA** : MA20 18.33 · MA50 17.83 · MA200 20.19  _(prix < MA20)_
- **Dist MA** : MA20 -2.5% · MA50 +0.3% · MA200 -11.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (776835 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
