# RGTI

**Generated** : 2026-09-02T00:28:55.111174+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $14.99  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $14.99 (+7.8% vs entrée) · entrée $13.91 · stop $12.85 · T1 $14.76 · R/R 0.8  
> ↳ P(T1 av. stop) 69 % · EV/risk -0.063 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $13.74–$14.08 (mid $13.91)
- Spot actuel : $14.99 (+7.8% au-dessus de la zone — repli à attendre)
- Stop : $12.85 (stop swing_plan-based (-14.27%))
- Targets : T1 $14.76 · R/R 0.8 | T2 $15.60 · R/R 1.59 | T3 $16.45 · R/R 2.4
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $12.85


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.38 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.27 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1253).
   - exécution **2.016 pt plus bas** dans le cas TYPIQUE (médiane), 12.954 au p90, **16.943 au pire**
   - perte réelle **19.597 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 14.27 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.017 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.104 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4236** [0.3518 ; 0.498] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.4463** [0.3945 ; 0.499] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4647** [0.4126 ; 0.5174] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.1 pt), swing (44.9 pt), deep (47.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.85 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 14.15 % contre 6.52 % aujourd'hui, rapport 2.17)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8215** (β de hausse 1.9909, asymétrie 0.9149) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.64× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.4032 sur atr_based (1.5 ATR, 10.586 %) — p(stop avant cible) 0.6179 [0.57 ; 0.67], R/R 1.534, perte reelle 16.129 % (gap inclus), CVaR 10.621 %, EV -4.1972 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2145 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.618, borne haute 0.668 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 60.2 % de la queue et il ne reste que -755.68 EUR a partager. Prix du risque -0.422 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.586 %) — p(stop avant cible) 0.6179 [0.57 ; 0.67], R/R 1.534, perte reelle 16.129 % (gap inclus), EV -4.1972 % — **REFUSE**
      - refuse : p_stop_first 0.618, borne haute 0.668 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.20 %) : P(cible) 20.1 % x 24.73 % + P(rien) 18.1 % x 4.41 % ne couvrent pas P(stop) 61.8 % x 16.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 1.96 ATR (stop 16.472 %) — p(stop avant cible) 0.3492 [0.30 ; 0.40], R/R 1.007, perte reelle 24.565 % (gap inclus), EV -2.7835 % — **REFUSE**
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.78 %) : P(cible) 22.8 % x 24.73 % + P(rien) 42.2 % x 0.35 % ne couvrent pas P(stop) 34.9 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.33 ATR (stop 19.057 %) — p(stop avant cible) 0.2566 [0.21 ; 0.30], R/R 0.792, perte reelle 31.213 % (gap inclus), EV -2.8358 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.84 %) : P(cible) 23.5 % x 24.73 % + P(rien) 50.8 % x -1.26 % ne couvrent pas P(stop) 25.7 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.764 %) — p(stop avant cible) 0.9047 [0.87 ; 0.93], R/R 6.229, perte reelle 3.971 % (gap inclus), EV -1.506 % — **REFUSE**
      - refuse : cible atteinte seulement 7.9 % du temps (< 15 %) meme a 10 seances : le R/R de 6.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.905, borne haute 0.932 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.51 %) : P(cible) 7.9 % x 24.73 % + P(rien) 1.7 % x 8.43 % ne couvrent pas P(stop) 90.5 % x 3.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.529 %) — p(stop avant cible) 0.8331 [0.79 ; 0.87], R/R 3.826, perte reelle 6.464 % (gap inclus), EV -2.0795 % — **REFUSE**
      - refuse : cible atteinte seulement 11.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.833, borne haute 0.870 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.08 %) : P(cible) 11.6 % x 24.73 % + P(rien) 5.1 % x 8.54 % ne couvrent pas P(stop) 83.3 % x 6.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.293 %) — p(stop avant cible) 0.7762 [0.73 ; 0.82], R/R 2.796, perte reelle 8.847 % (gap inclus), EV -2.857 % — **REFUSE**
      - refuse : cible atteinte seulement 13.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.776, borne haute 0.818 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.86 %) : P(cible) 13.8 % x 24.73 % + P(rien) 8.5 % x 6.87 % ne couvrent pas P(stop) 77.6 % x 8.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 7.057 %) — p(stop avant cible) 0.7134 [0.66 ; 0.76], R/R 2.117, perte reelle 11.681 % (gap inclus), EV -3.438 % — **REFUSE**
      - refuse : p_stop_first 0.713, borne haute 0.759 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.44 %) : P(cible) 16.8 % x 24.73 % + P(rien) 11.9 % x 6.30 % ne couvrent pas P(stop) 71.3 % x 11.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.821 %) — p(stop avant cible) 0.6596 [0.61 ; 0.71], R/R 1.849, perte reelle 13.376 % (gap inclus), EV -3.3255 % — **REFUSE**
      - refuse : p_stop_first 0.660, borne haute 0.708 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.33 %) : P(cible) 18.8 % x 24.73 % + P(rien) 15.2 % x 5.57 % ne couvrent pas P(stop) 66.0 % x 13.38 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 21.171 %) — p(stop avant cible) 0.2017 [0.16 ; 0.25], R/R 0.792, perte reelle 31.213 % (gap inclus), EV -1.5414 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.18 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.54 %) : P(cible) 24.0 % x 24.73 % + P(rien) 55.8 % x -2.12 % ne couvrent pas P(stop) 20.2 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 24.7 %) — p(stop avant cible) 0.1232 [0.09 ; 0.16], R/R 0.792, perte reelle 31.213 % (gap inclus), EV -0.0765 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 24.4 % x 24.73 % + P(rien) 63.2 % x -3.60 % ne couvrent pas P(stop) 12.3 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 28.228 %) — p(stop avant cible) 0.0766 [0.05 ; 0.11], R/R 0.792, perte reelle 31.213 % (gap inclus), EV 0.5343 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.23 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 31.757 %) — p(stop avant cible) 0.0479 [0.03 ; 0.07], R/R 0.779, perte reelle 31.757 % (gap inclus), EV 0.7478 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.76 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 35.285 %) — p(stop avant cible) 0.0287 [0.01 ; 0.05], R/R 0.701, perte reelle 35.285 % (gap inclus), EV 0.8382 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.28 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.814 %) — p(stop avant cible) 0.0142 [0.01 ; 0.03], R/R 0.637, perte reelle 38.814 % (gap inclus), EV 0.8802 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.81 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 42.343 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.584, perte reelle 42.343 % (gap inclus), EV 0.9429 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.34 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 45.871 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 0.539, perte reelle 45.871 % (gap inclus), EV 0.928 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.87 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 49.4 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 0.501, perte reelle 49.4 % (gap inclus), EV 0.9269 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.40 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 52.928 %) — p(stop avant cible) 0.0028 [0.00 ; 0.01], R/R 0.467, perte reelle 52.928 % (gap inclus), EV 0.921 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.93 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 56.457 %) — p(stop avant cible) 0.0022 [0.00 ; 0.01], R/R 0.438, perte reelle 56.457 % (gap inclus), EV 0.9466 % — **REFUSE**
      - refuse : R/R 0.44 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.46 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 14.99, ATR14 1.0579 (7.057 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.411 ATR = 2.9 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.353 % | 14.9371 | 92.15 % | 94.56 % | 95.66 % | 97.07 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.706 % | 14.8842 | 86.4 % | 91.23 % | 92.43 % | 94.94 % | 95.83 % | 97.43 % |
| 0.15 ATR | 1.059 % | 14.8313 | 80.97 % | 87.5 % | 89.1 % | 92.01 % | 93.9 % | 96.1 % |
| 0.2 ATR | 1.411 % | 14.7784 | 74.62 % | 82.96 % | 85.67 % | 88.88 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.764 % | 14.7255 | 68.58 % | 78.73 % | 81.84 % | 85.84 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.47 % | 14.6197 | 56.09 % | 68.55 % | 74.07 % | 79.68 % | 84.45 % | 89.63 % |
| 0.5 ATR | 3.529 % | 14.4611 | 41.19 % | 57.06 % | 64.98 % | 71.89 % | 79.27 % | 85.52 % |
| 0.75 ATR | 5.293 % | 14.1966 | 21.75 % | 39.01 % | 49.55 % | 59.15 % | 70.93 % | 79.26 % |
| 1.0 ATR | 7.057 % | 13.9321 | 9.57 % | 23.79 % | 33.6 % | 46.41 % | 61.89 % | 73.0 % |
| 1.25 ATR | 8.821 % | 13.6677 | 4.03 % | 14.52 % | 23.51 % | 36.91 % | 52.85 % | 65.09 % |
| 1.5 ATR | 10.586 % | 13.4032 | 1.71 % | 7.16 % | 13.72 % | 25.48 % | 43.09 % | 56.88 % |
| 2.0 ATR | 14.114 % | 12.8743 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.51 % | 40.86 % |
| 2.5 ATR | 17.643 % | 12.3454 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.43 % | 28.44 % |
| 3.0 ATR | 21.171 % | 11.8164 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.15 % |
| 4.0 ATR | 28.228 % | 10.7586 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 42.343 % | 8.6429 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.21 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.79 ATR | 2.02 ATR | 2.25 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.72 ATR | 1.87 ATR | 2.32 ATR | 2.65 ATR | 2.87 ATR | 3.58 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.462–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.529 %, prix 14.461), p(touche) 41.19 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.0 % des re-echantillons)
- **2 seance(s)** : plage utile 0.667–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.293 %, prix 14.1966), p(touche) 39.01 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.821–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.057 %, prix 13.9322), p(touche) 33.6 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.037–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.821 %, prix 13.6677), p(touche) 36.91 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.586 %, prix 13.4032), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 48.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.871–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (14.114 %, prix 12.8743), p(touche) 40.86 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.131 | EV/share : $-0.138 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 28 % | T3 16 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 30.0 | side 65.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.283% → cible +6.923% / stop −3.461%, p_fill 39%, n_eff≈15.6) : P(cible|rempli) **1%** · **EV/risk -0.131** (×p_fill ; si rempli -1.18% du capital)
  - **swing** (entrée dip −7.213% → cible +6.094% / stop −7.606%, p_fill 23%, n_eff≈11.4) : P(cible|rempli) **78%** · **EV/risk +0.100** (×p_fill ; si rempli +3.29% du capital)
  - **deep** (entrée dip −11.155% → cible +8.619% / stop −11.914%, p_fill 27%, n_eff≈14.3) : P(cible|rempli) **54%** · **EV/risk +0.016** (×p_fill ; si rempli +0.70% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→71% · +3.0%→52% · +5.0%→39% · +8.0%→12%
- Range intraday médian 7.5% (p90 11.55%) · excursion haute méd. +3.41% / basse méd. −2.8%
- Profil de vol intra : ouverture 5.358% vs midi 1.561% vs clôture 1.769% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 25% · trend ↑0%/↓0% ; spike-down 71% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. -0.096% ; recovery-V 33%
- **σ réalisé intraday** 4.181% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 46% / whipsaw 4%
- POC intraday (dernière séance, temps-au-prix) : 15.6212 (VA 15.5795–15.6837 ; dernier close 15.655)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 44% · rebond 73% · **stop −6.03%** sous le fill (sous le bruit) · cible +2.18% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.54% · baisse 60% (gap-down >1% 41% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −1.18% (p90 −2.88%) · haut méd +1.25% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.43% (p90 −3.8%) · haut méd +1.77% · range méd 3.62%
- Excursion ouverture 30min (n=160) : bas méd −1.75% (p90 −4.54%) · haut méd +2.09% · range méd 4.46%
- Excursion ouverture 60min (n=160) : bas méd −2.26% (p90 −5.61%) · haut méd +2.4% · range méd 5.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.66 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 82% (133/159) · gap 50% · délai 0.0min · rebond 63% (84/133) (MFE +2.31%)
   - −1.0% : fill 30min 65% · séance 72% (124/159) · gap 41% · délai 0.0min · rebond 64% (78/124) (MFE +1.67%)
   - −1.5% : fill 30min 60% · séance 68% (118/159) · gap 33% · délai 0.0min · rebond 65% (76/118) (MFE +2.06%)
   - −2.0% : fill 30min 53% · séance 61% (109/159) · gap 26% · délai 0.0min · rebond 65% (72/109) (MFE +1.85%)
   - −3.0% : fill 30min 45% · séance 56% (98/159) · gap 10% · délai 1.2min · rebond 67% (70/98) (MFE +2.07%)
   - −4.0% : fill 30min 34% · séance 44% (77/159) · gap 5% · délai 6.5min · rebond 73% (55/77) (MFE +2.18%)
   - −5.0% : fill 30min 18% · séance 37% (67/159) · gap 2% · délai 31.6min · rebond 55% (45/67) (MFE +1.57%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.39%) → stop au-delà de −1.67% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −2.79%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −2.92%) → stop au-delà de −2.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1151 jambes) : jambe baissière méd −1.28% (p90 −3.1%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (85 séances) :
      · −1.0% : fill 93% (82/85) · rebond 58% (47/82)
      · −2.0% : fill 84% (77/85) · rebond 62% (49/77)
      · −3.0% : fill 80% (73/85) · rebond 60% (49/73)
      · −4.0% : fill 68% (59/85) · rebond 70% (41/59)
      · −5.0% : fill 57% (52/85) · rebond 51% (34/52)
   - **flat** (15 séances) :
      · −1.0% : fill 96% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 74% (12/15) · rebond 85% (10/12)
      · −3.0% : fill 50% (7/15) · rebond 90% (5/7)
      · −4.0% : fill 34% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 21% (5/15) · rebond 87% (3/5)
   - **gap-up** (59 séances) :
      · −1.0% : fill 37% (28/59) · rebond 67% (19/28)
      · −2.0% : fill 25% (20/59) · rebond 64% (13/20)
      · −3.0% : fill 21% (18/59) · rebond 90% (16/18)
      · −4.0% : fill 13% (12/59) · rebond 84% (10/12)
      · −5.0% : fill 11% (10/59) · rebond 68% (8/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 73% si les 15 1res min sont vertes (81 cas) · 28% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 94% si début vert vs 9% si rouge (base 52% · écart 85 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **94%** · continue >prix actuel 56% ; creux résiduel méd -1.81% (q20 -2.86%) → **SL/trailing à −2.86%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.18% / q75 +4.16% → **scale +2.18% / runner +4.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **9%** (continue à baisser 70%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +1.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.01% .. +4.85%] · haut q95 +6.42% · bas q05 -6.02%
   - 60min (n=160) : retour [-5.37% .. +6.17%] · haut q95 +6.62% · bas q05 -6.65%
   - 2h (n=160) : retour [-6.32% .. +6.67%] · haut q95 +8.96% · bas q05 -7.37%
   - 4h (n=160) : retour [-6.61% .. +7.85%] · haut q95 +9.18% · bas q05 -7.8%
   - 6h (n=160) : retour [-7.25% .. +8.64%] · haut q95 +10.05% · bas q05 -8.49%
   - session (n=160) : retour [-7.11% .. +9.07%] · haut q95 +10.34% · bas q05 -8.62%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0% / strong 6.9%) · base = 11 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **30%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.66% / p90 2.45%) · ~4.39 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 15.0 min, n=47)
   - −1.0% → **83%** (reprise méd 35.0 min, n=29)
   - −1.5% → **84%** (reprise méd 94.96 min, n=17)
   - −2.0% → **86%** (reprise méd 54.27 min, n=9)
   - −3.0% → **67%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.45%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.3% (q75 +9.62% / q95 +9.99%), MFE méd +9.65% / q90 +11.14%
   - Échelle scale-out : +9.65% (33%) / +10.43% (33%) / +11.14% (34%)
- **DÉSARMER** : repli > **−2.45%** depuis le plus-haut = décay → P(retournement) **23%** (préavis méd 141.49 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.14% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.16%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 33.2  _(momentum baissier)_
- **ADX** : 14.2  _(pas de tendance nette)_
- **MACD** : hist -0.254  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 26.9%
- **ATR** : 1.06 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 44.7  _(transition)_
- **MA** : MA20 17.11 · MA50 16.71 · MA200 19.44  _(prix < MA20)_
- **Dist MA** : MA20 -12.4% · MA50 -10.3% · MA200 -22.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (778911 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
