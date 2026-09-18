# HOOD

**Generated** : 2026-09-18T05:50:47.592109+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $109.81  

> 🟡 **WAIT-FOR-DIP** — spot +1.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $109.81 (+1.7% vs entrée) · entrée $107.96 · stop $105.76 · T1 $112.37 · R/R 2.0  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk 0.088 _(réel 5 s)_ (GBM 0.046) · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.04% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $107.28–$108.64 (mid $107.96)
- Spot actuel : $109.81 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $105.76 (stop swing_plan-based (-9.99%))
- Targets : T1 $112.37 · R/R 2.0 | T2 $114.44 · R/R 2.95 | T3 $118.10 · R/R 4.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $105.76


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.02 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (9.99 %)** : le gap seul le franchit 0.479 % des séances (6 fois sur 1253).
   - exécution **1.521 pt plus bas** dans le cas TYPIQUE (médiane), 5.965 au p90, **7.795 au pire**
   - perte réelle **12.711 %** en moyenne _(tirée par la queue)_, jusqu'à **17.785 %** — au lieu des 9.99 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.013 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 6 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.416 % | p01 -7.308 % | pire -17.785 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5415** [0.4671 ; 0.6145] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4121** [0.3611 ; 0.4645] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3521** [0.3032 ; 0.4035] _(largeur 10.0 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.3 pt), swing (41.5 pt), deep (42.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-6.19 %** | CVaR **-9.11 %** | vol 4.4 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 1.85 % contre 4.70 % aujourd'hui, rapport 0.39)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.55 % vs -14.36 % si l'on extrapolait par √5 _(rapport 1.013 ; < 1 = le √5 surestime)_
- **β de baisse : 1.7517** (β de hausse 1.5961, asymétrie 1.0975) vs IWM — 603 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.44× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 97.1276 sur support (1.32 ATR, 11.549 %) — p(stop avant cible) 0.2976 [0.25 ; 0.35], R/R 1.131, perte reelle 14.605 % (gap inclus), CVaR 11.556 %, EV 1.6142 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.32 ATR (stop 11.549 %) — p(stop avant cible) 0.2976 [0.25 ; 0.35], R/R 1.131, perte reelle 14.605 % (gap inclus), EV 1.6142 % — **REFUSE**
      - refuse : R/R 1.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - 🟢 support a 2.66 ATR (stop 19.964 %) — p(stop avant cible) 0.0829 [0.06 ; 0.12], R/R 0.828, perte reelle 19.964 % (gap inclus), EV 2.7294 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.96 % > budget 12.00 %
   - 🟢 support a 4.48 ATR (stop 31.356 %) — p(stop avant cible) 0.0191 [0.01 ; 0.04], R/R 0.527, perte reelle 31.356 % (gap inclus), EV 2.7693 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.36 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.57 %) — p(stop avant cible) 0.8867 [0.85 ; 0.92], R/R 4.931, perte reelle 3.351 % (gap inclus), EV -1.3987 % — **REFUSE**
      - refuse : cible atteinte seulement 8.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.887, borne haute 0.917 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.40 %) : P(cible) 8.3 % x 16.52 % + P(rien) 3.1 % x 6.73 % ne couvrent pas P(stop) 88.7 % x 3.35 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.141 %) — p(stop avant cible) 0.7485 [0.70 ; 0.79], R/R 3.121, perte reelle 5.294 % (gap inclus), EV -0.5494 % — **REFUSE**
      - refuse : p_stop_first 0.749, borne haute 0.792 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.55 %) : P(cible) 17.4 % x 16.52 % + P(rien) 7.8 % x 6.98 % ne couvrent pas P(stop) 74.9 % x 5.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.711 %) — p(stop avant cible) 0.6394 [0.59 ; 0.69], R/R 2.192, perte reelle 7.539 % (gap inclus), EV -0.4326 % — **REFUSE**
      - refuse : p_stop_first 0.639, borne haute 0.689 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.19 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 22.0 % x 16.52 % + P(rien) 14.1 % x 5.34 % ne couvrent pas P(stop) 63.9 % x 7.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.282 %) — p(stop avant cible) 0.5502 [0.50 ; 0.60], R/R 1.69, perte reelle 9.781 % (gap inclus), EV -0.2145 % — **REFUSE**
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.69 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.21 %) : P(cible) 25.2 % x 16.52 % + P(rien) 19.7 % x 5.05 % ne couvrent pas P(stop) 55.0 % x 9.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.32 ATR (stop 10.199 %) — p(stop avant cible) 0.3472 [0.30 ; 0.40], R/R 1.3, perte reelle 12.711 % (gap inclus), EV 1.5513 % — **REFUSE**
      - refuse : R/R 1.30 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 12.563 %) — p(stop avant cible) 0.2606 [0.22 ; 0.31], R/R 1.036, perte reelle 15.955 % (gap inclus), EV 1.8339 % — **REFUSE**
      - refuse : R/R 1.04 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.57 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 14.134 %) — p(stop avant cible) 0.2105 [0.17 ; 0.26], R/R 0.929, perte reelle 17.785 % (gap inclus), EV 1.9942 % — **REFUSE**
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.14 % > budget 12.00 %
   - 🟢 grid_snapped a 2.66 ATR (stop 18.613 %) — p(stop avant cible) 0.1041 [0.08 ; 0.14], R/R 0.888, perte reelle 18.613 % (gap inclus), EV 2.7449 % — **REFUSE**
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.61 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 21.986 %) — p(stop avant cible) 0.064 [0.04 ; 0.09], R/R 0.752, perte reelle 21.986 % (gap inclus), EV 2.7523 % — **REFUSE**
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.99 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 25.127 %) — p(stop avant cible) 0.035 [0.02 ; 0.06], R/R 0.658, perte reelle 25.127 % (gap inclus), EV 2.767 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.13 % > budget 12.00 %
   - 🟢 grid_snapped a 4.48 ATR (stop 30.006 %) — p(stop avant cible) 0.0236 [0.01 ; 0.04], R/R 0.551, perte reelle 30.006 % (gap inclus), EV 2.7541 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.01 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 34.549 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.478, perte reelle 34.549 % (gap inclus), EV 2.8891 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.55 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 37.69 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.438, perte reelle 37.69 % (gap inclus), EV 2.8962 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.69 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 40.831 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.405, perte reelle 40.831 % (gap inclus), EV 2.9171 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.83 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 43.972 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.376, perte reelle 43.972 % (gap inclus), EV 2.9171 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 43.97 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.113 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.351, perte reelle 47.113 % (gap inclus), EV 2.9171 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.11 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 50.254 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.329, perte reelle 50.254 % (gap inclus), EV 2.9171 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.25 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 109.81, ATR14 6.8979 (6.282 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.374 ATR = 2.349 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.314 % | 109.4651 | 92.95 % | 95.06 % | 95.96 % | 96.46 % | 97.05 % | 98.05 % |
| 0.1 ATR | 0.628 % | 109.1202 | 85.5 % | 90.32 % | 92.03 % | 93.53 % | 94.61 % | 96.41 % |
| 0.15 ATR | 0.942 % | 108.7753 | 77.54 % | 85.08 % | 87.79 % | 90.09 % | 92.48 % | 95.07 % |
| 0.2 ATR | 1.256 % | 108.4304 | 71.5 % | 79.94 % | 83.55 % | 86.75 % | 90.24 % | 93.22 % |
| 0.25 ATR | 1.57 % | 108.0855 | 64.55 % | 74.19 % | 78.91 % | 83.22 % | 87.6 % | 90.86 % |
| 0.35 ATR | 2.199 % | 107.3957 | 52.47 % | 65.22 % | 71.75 % | 77.45 % | 83.33 % | 87.89 % |
| 0.5 ATR | 3.141 % | 106.361 | 37.16 % | 53.33 % | 60.95 % | 68.05 % | 76.32 % | 82.44 % |
| 0.75 ATR | 4.711 % | 104.6365 | 19.64 % | 36.19 % | 45.81 % | 55.41 % | 65.45 % | 73.2 % |
| 1.0 ATR | 6.282 % | 102.9121 | 9.26 % | 22.98 % | 32.59 % | 43.58 % | 54.67 % | 65.61 % |
| 1.25 ATR | 7.852 % | 101.1876 | 4.83 % | 14.52 % | 22.3 % | 33.27 % | 46.54 % | 59.03 % |
| 1.5 ATR | 9.423 % | 99.4631 | 2.42 % | 9.88 % | 16.25 % | 26.79 % | 39.53 % | 53.39 % |
| 2.0 ATR | 12.563 % | 96.0141 | 0.5 % | 3.83 % | 7.27 % | 15.37 % | 29.37 % | 44.05 % |
| 2.5 ATR | 15.704 % | 92.5652 | 0.1 % | 1.51 % | 3.83 % | 8.19 % | 21.14 % | 34.6 % |
| 3.0 ATR | 18.845 % | 89.1162 | 0.0 % | 0.71 % | 2.32 % | 5.26 % | 15.35 % | 26.59 % |
| 4.0 ATR | 25.127 % | 82.2183 | 0.0 % | 0.4 % | 0.91 % | 2.22 % | 6.91 % | 14.89 % |
| 6.0 ATR | 37.69 % | 68.4224 | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.32 % | 4.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.17 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.74 ATR | 0.98 ATR | 1.24 ATR |
| **2 s.** | 0.24 ATR | 0.55 ATR | 0.62 ATR | 0.81 ATR | 0.96 ATR | 1.09 ATR | 1.49 ATR | 1.90 ATR |
| **3 s.** | 0.30 ATR | 0.68 ATR | 0.77 ATR | 0.99 ATR | 1.18 ATR | 1.34 ATR | 1.85 ATR | 2.33 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.26 ATR | 1.58 ATR | 1.80 ATR | 2.37 ATR | 3.09 ATR |
| **10 s.** | 0.53 ATR | 1.14 ATR | 1.30 ATR | 1.82 ATR | 2.27 ATR | 2.60 ATR | 3.63 ATR | 4.68 ATR |
| **20 s.** | 0.70 ATR | 1.68 ATR | 1.95 ATR | 2.60 ATR | 3.14 ATR | 3.56 ATR | 4.95 ATR | 5.93 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.423–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.621–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.711 %, prix 104.6368), p(touche) 36.19 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.765–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.282 %, prix 102.9117), p(touche) 32.59 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (61.5 % des re-echantillons)
- **5 seance(s)** : plage utile 0.97–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.282 %, prix 102.9117), p(touche) 43.58 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 59.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.305–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.423 %, prix 99.4626), p(touche) 39.53 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.949–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (12.563 %, prix 96.0146), p(touche) 44.05 % (en stress 97.96 %)  ✅ optimum identifie (63.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.046 | EV/share : $0.100 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.028 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.7 | bear 44.0 | side 33.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 329.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.684% → cible +4.08% / stop −2.04%, p_fill 64%, n_eff≈26.4) : P(cible|rempli) **16%** · **EV/risk +0.088** (×p_fill ; si rempli +0.28% du capital)
  - **swing** (entrée dip −3.708% → cible +8.229% / stop −6.523%, p_fill 46%, n_eff≈19.7) : P(cible|rempli) **48%** · **EV/risk +0.210** (×p_fill ; si rempli +2.98% du capital)
  - **deep** (entrée dip −5.727% → cible +17.831% / stop −9.995%, p_fill 34%, n_eff≈17.0) : P(cible|rempli) **37%** · **EV/risk +0.144** (×p_fill ; si rempli +4.23% du capital)
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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 50.0  _(neutre)_
- **ADX** : 18.9  _(pas de tendance nette)_
- **MACD** : hist -0.87  _(bearish_recent)_
- **BB** : %B 0.49 · largeur 25.0%
- **ATR** : 6.9 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.03  _(neutre)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 51.9  _(transition)_
- **MA** : MA20 110.06 · MA50 103.08 · MA200 94.92  _(prix < MA20)_
- **Dist MA** : MA20 -0.2% · MA50 +6.5% · MA200 +15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (754902 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
