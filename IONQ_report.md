# IONQ

**Generated** : 2026-08-28T00:28:28.053952+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $42.46  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $42.46 (+2.1% vs entrée) · entrée $41.57 · stop $40.07 · T1 $44.56 · R/R 1.99  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ (GBM -0.031) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.61% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $41.32–$41.81 (mid $41.57)
- Spot actuel : $42.46 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : $40.07 (stop swing_plan-based (-11.08%))
- Targets : T1 $44.56 · R/R 1.99 | T2 $44.88 · R/R 2.21 | T3 $45.19 · R/R 2.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $40.07


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.78 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.08 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **0.866 pt plus bas** dans le cas TYPIQUE (médiane), 8.797 au p90, **10.779 au pire**
   - perte réelle **15.082 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 11.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0096 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.035 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4148** [0.3433 ; 0.4891] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4981** [0.4456 ; 0.5506] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4625** [0.4104 ; 0.5152] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.7 pt), swing (39.3 pt), deep (37.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-9.0 %** | CVaR **-12.13 %** | vol 6.96 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 3.71 % contre 5.98 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -18.23 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.917 ; < 1 = le √5 surestime)_
- **β de baisse : 2.216** (β de hausse 1.9941, asymétrie 1.1113) vs IWM — 601 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 37.1794 sur grid_snapped (1.63 ATR, 12.437 %) — p(stop avant cible) 0.4514 [0.40 ; 0.50], R/R 1.172, perte reelle 21.859 % (gap inclus), CVaR 12.445 %, EV -3.3258 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.037 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 12.44 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 27 des 27 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 52.8 % de la queue et il ne reste que -406.12 EUR a partager. Prix du risque -0.191 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.98 ATR (stop 9.764 %) — p(stop avant cible) 0.5778 [0.53 ; 0.63], R/R 1.835, perte reelle 13.966 % (gap inclus), EV -1.6349 % — **REFUSE**
      - refuse : p_stop_first 0.578, borne haute 0.629 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.63 %) : P(cible) 20.4 % x 25.63 % + P(rien) 21.8 % x 5.51 % ne couvrent pas P(stop) 57.8 % x 13.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.63 ATR (stop 13.963 %) — p(stop avant cible) 0.4038 [0.35 ; 0.46], R/R 1.172, perte reelle 21.859 % (gap inclus), EV -2.5073 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.51 %) : P(cible) 21.8 % x 25.63 % + P(rien) 37.8 % x 1.94 % ne couvrent pas P(stop) 40.4 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.03 ATR (stop 22.96 %) — p(stop avant cible) 0.1496 [0.12 ; 0.19], R/R 1.116, perte reelle 22.96 % (gap inclus), EV 1.1797 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.96 % > budget 12.00 %
   - 🟢 support a 4.56 ATR (stop 32.828 %) — p(stop avant cible) 0.0274 [0.01 ; 0.05], R/R 0.781, perte reelle 32.828 % (gap inclus), EV 1.0862 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.83 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.611 %) — p(stop avant cible) 0.9217 [0.89 ; 0.95], R/R 7.525, perte reelle 3.406 % (gap inclus), EV -1.431 % — **REFUSE**
      - refuse : cible atteinte seulement 5.8 % du temps (< 15 %) meme a 10 seances : le R/R de 7.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.922, borne haute 0.947 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.43 %) : P(cible) 5.8 % x 25.63 % + P(rien) 2.1 % x 11.21 % ne couvrent pas P(stop) 92.2 % x 3.41 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.221 %) — p(stop avant cible) 0.844 [0.80 ; 0.88], R/R 4.967, perte reelle 5.16 % (gap inclus), EV -1.1302 % — **REFUSE**
      - refuse : cible atteinte seulement 10.9 % du temps (< 15 %) meme a 10 seances : le R/R de 4.97 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.844, borne haute 0.879 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 10.9 % x 25.63 % + P(rien) 4.7 % x 9.28 % ne couvrent pas P(stop) 84.4 % x 5.16 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.98 ATR (stop 8.238 %) — p(stop avant cible) 0.6374 [0.59 ; 0.69], R/R 2.252, perte reelle 11.379 % (gap inclus), EV -1.1037 % — **REFUSE**
      - refuse : p_stop_first 0.637, borne haute 0.687 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.10 %) : P(cible) 19.7 % x 25.63 % + P(rien) 16.6 % x 6.63 % ne couvrent pas P(stop) 63.7 % x 11.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.63 ATR (stop 12.437 %) — p(stop avant cible) 0.4514 [0.40 ; 0.50], R/R 1.172, perte reelle 21.859 % (gap inclus), EV -3.3258 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.44 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 21.7 % x 25.63 % + P(rien) 33.2 % x 2.98 % ne couvrent pas P(stop) 45.1 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 16.105 %) — p(stop avant cible) 0.3195 [0.27 ; 0.37], R/R 1.172, perte reelle 21.859 % (gap inclus), EV -1.1837 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 22.1 % x 25.63 % + P(rien) 46.0 % x 0.32 % ne couvrent pas P(stop) 31.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 17.716 %) — p(stop avant cible) 0.2794 [0.23 ; 0.33], R/R 1.172, perte reelle 21.859 % (gap inclus), EV -0.3448 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 23.0 % x 25.63 % + P(rien) 49.1 % x -0.25 % ne couvrent pas P(stop) 27.9 % x 21.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.03 ATR (stop 21.433 %) — p(stop avant cible) 0.187 [0.15 ; 0.23], R/R 1.172, perte reelle 21.859 % (gap inclus), EV 0.9992 % — **REFUSE**
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.43 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.769 %) — p(stop avant cible) 0.0981 [0.07 ; 0.13], R/R 0.995, perte reelle 25.769 % (gap inclus), EV 1.1613 % — **REFUSE**
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.77 % > budget 12.00 %
   - 🟢 grid_snapped a 4.56 ATR (stop 31.301 %) — p(stop avant cible) 0.0469 [0.03 ; 0.07], R/R 0.819, perte reelle 31.301 % (gap inclus), EV 1.0511 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.30 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.432 %) — p(stop avant cible) 0.0155 [0.01 ; 0.03], R/R 0.723, perte reelle 35.432 % (gap inclus), EV 1.1453 % — **REFUSE**
      - refuse : R/R 0.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.43 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 38.653 %) — p(stop avant cible) 0.0094 [0.00 ; 0.02], R/R 0.663, perte reelle 38.653 % (gap inclus), EV 1.1486 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.65 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 41.874 %) — p(stop avant cible) 0.0037 [0.00 ; 0.01], R/R 0.612, perte reelle 41.874 % (gap inclus), EV 1.1597 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.87 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.095 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.568, perte reelle 45.095 % (gap inclus), EV 1.1629 % — **REFUSE**
      - refuse : R/R 0.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.10 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.316 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.53, perte reelle 48.316 % (gap inclus), EV 1.1839 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.32 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.538 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.497, perte reelle 51.538 % (gap inclus), EV 1.2015 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.54 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 42.46, ATR14 2.7354 (6.442 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 2.461 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.322 % | 42.3232 | 93.55 % | 95.26 % | 95.96 % | 97.47 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.644 % | 42.1865 | 86.0 % | 91.03 % | 92.03 % | 94.54 % | 96.04 % | 96.92 % |
| 0.15 ATR | 0.966 % | 42.0497 | 79.25 % | 86.19 % | 88.29 % | 91.61 % | 93.8 % | 95.79 % |
| 0.2 ATR | 1.288 % | 41.9129 | 71.8 % | 80.44 % | 84.26 % | 88.47 % | 91.06 % | 93.74 % |
| 0.25 ATR | 1.611 % | 41.7762 | 65.76 % | 76.61 % | 80.73 % | 85.84 % | 88.82 % | 92.2 % |
| 0.35 ATR | 2.255 % | 41.5026 | 53.27 % | 67.54 % | 74.07 % | 79.27 % | 84.15 % | 88.6 % |
| 0.5 ATR | 3.221 % | 41.0923 | 38.07 % | 54.74 % | 62.26 % | 70.98 % | 78.56 % | 84.8 % |
| 0.75 ATR | 4.832 % | 40.4085 | 22.26 % | 38.91 % | 48.23 % | 58.75 % | 68.9 % | 76.9 % |
| 1.0 ATR | 6.442 % | 39.7246 | 9.87 % | 24.5 % | 34.81 % | 45.8 % | 57.83 % | 68.17 % |
| 1.25 ATR | 8.053 % | 39.0408 | 3.63 % | 14.31 % | 24.12 % | 34.68 % | 50.0 % | 62.01 % |
| 1.5 ATR | 9.663 % | 38.357 | 1.01 % | 7.06 % | 15.84 % | 25.58 % | 41.16 % | 56.16 % |
| 2.0 ATR | 12.884 % | 36.9893 | 0.1 % | 1.92 % | 4.94 % | 14.56 % | 28.56 % | 44.87 % |
| 2.5 ATR | 16.105 % | 35.6216 | 0.0 % | 0.2 % | 1.21 % | 5.76 % | 18.19 % | 33.78 % |
| 3.0 ATR | 19.327 % | 34.2539 | 0.0 % | 0.1 % | 0.4 % | 2.63 % | 11.38 % | 25.87 % |
| 4.0 ATR | 25.769 % | 31.5186 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 38.653 % | 26.0479 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.00 ATR | 1.20 ATR |
| **2 s.** | 0.27 ATR | 0.57 ATR | 0.65 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.04 ATR | 1.23 ATR | 1.37 ATR | 1.77 ATR | 2.00 ATR |
| **5 s.** | 0.43 ATR | 0.92 ATR | 1.02 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.62 ATR |
| **10 s.** | 0.59 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.17 ATR | 2.41 ATR | 3.16 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.77 ATR | 1.99 ATR | 2.55 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.654–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.832 %, prix 40.4083), p(touche) 38.91 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.81–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.442 %, prix 39.7247), p(touche) 34.81 % (en stress 92.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.018–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.053 %, prix 39.0407), p(touche) 34.68 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.391–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.663 %, prix 38.3571), p(touche) 41.16 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.884 %, prix 36.9895), p(touche) 44.87 % (en stress 98.98 %)  ✅ optimum identifie (68.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : $-0.046 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 31 % | T3 31 %
- Kelly (position) : f* 0.111 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 69.9 | bear 22.9 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.11% → cible +7.213% / stop −3.606%, p_fill 57%, n_eff≈25.7) : P(cible|rempli) **2%** · **EV/risk -0.043** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −4.638% → cible +6.503% / stop −6.755%, p_fill 39%, n_eff≈22.1) : P(cible|rempli) **40%** · **EV/risk -0.096** (×p_fill ; si rempli -1.67% du capital)
  - **deep** (entrée dip −7.167% → cible +9.197% / stop −10.409%, p_fill 38%, n_eff≈24.2) : P(cible|rempli) **31%** · **EV/risk -0.151** (×p_fill ; si rempli -4.18% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→68% · +3.0%→59% · +5.0%→32% · +8.0%→15%
- Range intraday médian 7.64% (p90 12.17%) · excursion haute méd. +3.66% / basse méd. −2.75%
- Profil de vol intra : ouverture 5.31% vs midi 1.497% vs clôture 1.685% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr 0.011)_ ; drift intra méd. 0.322% ; recovery-V 29%
- **σ réalisé intraday** 4.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 50% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 44.7594 (VA 44.1094–45.0844 ; dernier close 44.85)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 85% · **stop −5.07%** sous le fill (sous le bruit) · cible +2.77% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. -0.31% · baisse 53% (gap-down >1% 36% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −1.16% (p90 −2.83%) · haut méd +1.33% · range méd 2.79%
- Excursion ouverture 15min (n=160) : bas méd −1.59% (p90 −4.01%) · haut méd +1.52% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.91% (p90 −5.15%) · haut méd +2.05% · range méd 4.53%
- Excursion ouverture 60min (n=160) : bas méd −2.25% (p90 −5.61%) · haut méd +2.32% · range méd 5.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 44.86 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 82% (133/159) · gap 46% · délai 0.0min · rebond 62% (86/133) (MFE +1.86%)
   - −1.0% : fill 30min 69% · séance 75% (125/159) · gap 36% · délai 0.0min · rebond 72% (91/125) (MFE +2.35%)
   - −1.5% : fill 30min 62% · séance 68% (117/159) · gap 31% · délai 0.0min · rebond 69% (81/117) (MFE +2.07%)
   - −2.0% : fill 30min 55% · séance 63% (108/159) · gap 18% · délai 0.1min · rebond 72% (76/108) (MFE +2.31%)
   - −3.0% : fill 30min 46% · séance 54% (93/159) · gap 8% · délai 6.3min · rebond 75% (69/93) (MFE +2.5%)
   - −4.0% : fill 30min 26% · séance 43% (76/159) · gap 6% · délai 21.5min · rebond 73% (59/76) (MFE +2.36%)
   - −5.0% : fill 30min 18% · séance 35% (64/159) · gap 3% · délai 24.8min · rebond 85% (55/64) (MFE +2.77%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.89%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −3.23%) → stop au-delà de −2.34% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.82% (p90 −2.73%) → stop au-delà de −1.84% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1125 jambes) : jambe baissière méd −1.31% (p90 −3.14%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 100% (78/78) · rebond 73% (58/78)
      · −2.0% : fill 90% (72/78) · rebond 77% (55/72)
      · −3.0% : fill 77% (62/78) · rebond 76% (47/62)
      · −4.0% : fill 60% (48/78) · rebond 74% (38/48)
      · −5.0% : fill 48% (40/78) · rebond 80% (33/40)
   - **flat** (15 séances) :
      · −1.0% : fill 78% (12/15) · rebond 65% (7/12)
      · −2.0% : fill 69% (11/15) · rebond 79% (6/11)
      · −3.0% : fill 62% (9/15) · rebond 62% (6/9)
      · −4.0% : fill 54% (8/15) · rebond 53% (4/8)
      · −5.0% : fill 39% (7/15) · rebond 95% (6/7)
   - **gap-up** (66 séances) :
      · −1.0% : fill 42% (35/66) · rebond 73% (26/35)
      · −2.0% : fill 26% (25/66) · rebond 49% (15/25)
      · −3.0% : fill 23% (22/66) · rebond 76% (16/22)
      · −4.0% : fill 20% (20/66) · rebond 80% (17/20)
      · −5.0% : fill 17% (17/66) · rebond 98% (16/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 58% si les 15 1res min sont vertes (80 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 70% si début vert vs 22% si rouge (base 46% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 234min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **70%** · continue >prix actuel 43% ; creux résiduel méd -2.94% (q20 -4.58%) → **SL/trailing à −4.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +4.69% → **scale +2.03% / runner +4.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **22%** (continue à baisser 54%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +2.07% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.1% .. +6.84%] · haut q95 +7.86% · bas q05 -5.64%
   - 60min (n=160) : retour [-4.98% .. +6.12%] · haut q95 +8.41% · bas q05 -6.18%
   - 2h (n=160) : retour [-6.38% .. +7.84%] · haut q95 +9.04% · bas q05 -7.04%
   - 4h (n=160) : retour [-7.04% .. +7.21%] · haut q95 +10.16% · bas q05 -8.09%
   - 6h (n=160) : retour [-7.2% .. +8.45%] · haut q95 +10.89% · bas q05 -8.3%
   - session (n=160) : retour [-6.6% .. +8.94%] · haut q95 +11.03% · bas q05 -8.35%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.7)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 15% vs absente 4% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.29% (p75 2.28% / p90 3.82%) · ~3.0 replis/séance, durée méd 69.04 min. P(nouveau plus-haut après repli) :
   - −0.5% → **85%** (reprise méd 24.37 min, n=47)
   - −1.0% → **78%** (reprise méd 68.85 min, n=30)
   - −1.5% → **68%** (reprise méd 81.24 min, n=16)
   - −2.0% → **67%** (reprise méd 84.17 min, n=12)
   - −3.0% → **75%** (reprise méd 175.72 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.82%** (p90, défaut prudent ; serré/agressif −2.28%) ; extension open→close méd +8.23% (q75 +10.03% / q95 +16.4%), MFE méd +10.28% / q90 +13.1%
   - Échelle scale-out : +10.28% (33%) / +11.83% (33%) / +13.1% (34%)
- **DÉSARMER** : repli > **−3.82%** depuis le plus-haut = décay → P(retournement) **30%** (préavis méd 235.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.1% : P(retournement après) 0% (mèche méd 3.44%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.52%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 46.0  _(neutre)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -0.043  _(bearish_recent)_
- **BB** : %B 0.5 · largeur 25.0%
- **ATR** : 2.74 (12.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.014  _(neutre)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 59.4  _(transition)_
- **MA** : MA20 42.49 · MA50 43.19 · MA200 44.56  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 -1.7% · MA200 -4.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (840235 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
