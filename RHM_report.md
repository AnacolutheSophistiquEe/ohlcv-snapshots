# RHM

**Generated** : 2026-08-28T21:35:48.990424+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1154.60  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot €1154.60 (+0.5% vs entrée) · entrée €1148.90 · stop €1125.92 · T1 €1161.56 · R/R 0.55  
> ↳ P(T1 av. stop) 61 % _(réel 5 s)_ · EV/risk 0.016 _(réel 5 s)_ (GBM 0.093) · ¼-Kelly 0.044 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1146.37–€1151.43 (mid €1148.90)
- Spot actuel : €1154.60 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €1125.92 (stop swing_plan-based (-4.43%))
- Targets : T1 €1161.56 · R/R 0.55 | T2 €1174.22 · R/R 1.1 | T3 €1186.88 · R/R 1.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1125.92


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.43 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **0.601 pt plus bas** dans le cas TYPIQUE (médiane), 9.253 au p90, **17.999 au pire**
   - perte réelle **7.856 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 4.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0188 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.562 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3229** [0.2566 ; 0.395] _(largeur 13.8 pt, n_eff 173.1)_
   - swing : **0.4026** [0.3519 ; 0.4549] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.4003** [0.3497 ; 0.4526] _(largeur 10.3 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 29.5 observations effectives », dont la borne haute a 95 % vaut environ 10.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (34.6 pt), deep (27.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.86 %** | CVaR **-6.73 %** | vol 2.97 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 2.04 % contre 3.33 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.61 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.847 ; < 1 = le √5 surestime)_
- **β de baisse : 0.4974** (β de hausse 0.5828, asymétrie 0.8535) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.107× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 1019.55 sur atr_grid (3.5 ATR, 11.697 %) — p(stop avant cible) 0.2359 [0.19 ; 0.28], R/R 1.466, perte reelle 22.429 % (gap inclus), CVaR 11.705 %, EV -2.8153 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 31 des 31 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 43.2 % de la queue et il ne reste que -839.13 EUR a partager. Prix du risque -0.27 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.69 ATR (stop 4.428 %) — p(stop avant cible) 0.6148 [0.56 ; 0.67], R/R 4.186, perte reelle 7.856 % (gap inclus), EV -1.9086 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.615, borne haute 0.665 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 0.3 % x 32.88 % + P(rien) 38.2 % x 7.41 % ne couvrent pas P(stop) 61.5 % x 7.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.08 ATR (stop 5.732 %) — p(stop avant cible) 0.5294 [0.48 ; 0.58], R/R 2.714, perte reelle 12.114 % (gap inclus), EV -3.3696 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.529, borne haute 0.582 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.37 %) : P(cible) 0.4 % x 32.88 % + P(rien) 46.7 % x 6.24 % ne couvrent pas P(stop) 52.9 % x 12.11 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🔴 support a 1.44 ATR (stop 6.917 %) — p(stop avant cible) 0.4353 [0.38 ; 0.49], R/R 2.172, perte reelle 15.141 % (gap inclus), EV -3.5461 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.59 ATR du spot — compartiment <1, mesure a 45.2 % de casse (IC clusterise [0.423 ; 0.481] sur 1194 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.55 %) : P(cible) 0.5 % x 32.88 % + P(rien) 56.0 % x 5.16 % ne couvrent pas P(stop) 43.5 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 5.85 ATR (stop 21.675 %) — p(stop avant cible) 0.0371 [0.02 ; 0.06], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -0.3586 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.5 % x 32.88 % + P(rien) 95.8 % x 0.33 % ne couvrent pas P(stop) 3.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 0.835 %) — p(stop avant cible) 0.9291 [0.90 ; 0.95], R/R 15.771, perte reelle 2.085 % (gap inclus), EV -1.1507 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 15.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.929, borne haute 0.953 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.15 %) : P(cible) 0.0 % x 32.88 % + P(rien) 7.1 % x 11.11 % ne couvrent pas P(stop) 92.9 % x 2.08 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 0.69 ATR (stop 3.311 %) — p(stop avant cible) 0.704 [0.65 ; 0.75], R/R 6.087, perte reelle 5.402 % (gap inclus), EV -1.3102 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 6.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.704, borne haute 0.750 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 0.2 % x 32.88 % + P(rien) 29.4 % x 8.25 % ne couvrent pas P(stop) 70.4 % x 5.40 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 7.519 %) — p(stop avant cible) 0.3949 [0.34 ; 0.45], R/R 2.172, perte reelle 15.141 % (gap inclus), EV -2.998 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.00 %) : P(cible) 0.5 % x 32.88 % + P(rien) 60.0 % x 4.70 % ne couvrent pas P(stop) 39.5 % x 15.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 8.355 %) — p(stop avant cible) 0.3745 [0.32 ; 0.43], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -5.4528 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.45 %) : P(cible) 0.5 % x 32.88 % + P(rien) 62.1 % x 4.49 % ne couvrent pas P(stop) 37.5 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 9.19 %) — p(stop avant cible) 0.3369 [0.29 ; 0.39], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -4.6616 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.66 %) : P(cible) 0.5 % x 32.88 % + P(rien) 65.8 % x 4.16 % ne couvrent pas P(stop) 33.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 10.026 %) — p(stop avant cible) 0.2907 [0.24 ; 0.34], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -3.8384 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.84 %) : P(cible) 0.5 % x 32.88 % + P(rien) 70.5 % x 3.58 % ne couvrent pas P(stop) 29.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 11.697 %) — p(stop avant cible) 0.2359 [0.19 ; 0.28], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -2.8153 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.82 %) : P(cible) 0.5 % x 32.88 % + P(rien) 75.9 % x 3.05 % ne couvrent pas P(stop) 23.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 13.368 %) — p(stop avant cible) 0.1745 [0.14 ; 0.22], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -1.9327 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.93 %) : P(cible) 0.5 % x 32.88 % + P(rien) 82.1 % x 2.22 % ne couvrent pas P(stop) 17.4 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 15.039 %) — p(stop avant cible) 0.1334 [0.10 ; 0.17], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -1.3046 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 0.5 % x 32.88 % + P(rien) 86.2 % x 1.77 % ne couvrent pas P(stop) 13.3 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 16.71 %) — p(stop avant cible) 0.107 [0.08 ; 0.14], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -1.0188 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.02 %) : P(cible) 0.5 % x 32.88 % + P(rien) 88.8 % x 1.38 % ne couvrent pas P(stop) 10.7 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 18.381 %) — p(stop avant cible) 0.0706 [0.05 ; 0.10], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -0.6477 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.38 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.65 %) : P(cible) 0.5 % x 32.88 % + P(rien) 92.5 % x 0.84 % ne couvrent pas P(stop) 7.1 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 5.85 ATR (stop 20.559 %) — p(stop avant cible) 0.0463 [0.03 ; 0.07], R/R 1.466, perte reelle 22.429 % (gap inclus), EV -0.491 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.56 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.5 % x 32.88 % + P(rien) 94.9 % x 0.41 % ne couvrent pas P(stop) 4.6 % x 22.43 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 23.393 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 1.406, perte reelle 23.393 % (gap inclus), EV -0.1511 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.39 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.15 %) : P(cible) 0.5 % x 32.88 % + P(rien) 98.4 % x -0.04 % ne couvrent pas P(stop) 1.1 % x 23.39 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 25.064 %) — p(stop avant cible) 0.007 [0.00 ; 0.02], R/R 1.312, perte reelle 25.064 % (gap inclus), EV -0.1636 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.5 % x 32.88 % + P(rien) 98.8 % x -0.15 % ne couvrent pas P(stop) 0.7 % x 25.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 26.735 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 1.23, perte reelle 26.735 % (gap inclus), EV -0.1406 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.5 % x 32.88 % + P(rien) 98.9 % x -0.13 % ne couvrent pas P(stop) 0.6 % x 26.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 1154.6, ATR14 38.5857 (3.342 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.39 ATR = 1.303 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.167 % | 1152.6707 | 89.25 % | 92.1 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.334 % | 1150.7414 | 83.23 % | 87.76 % | 89.72 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.501 % | 1148.8121 | 76.13 % | 82.82 % | 85.57 % | 88.22 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.668 % | 1146.8828 | 69.63 % | 78.38 % | 81.52 % | 85.15 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.835 % | 1144.9535 | 62.13 % | 72.66 % | 76.58 % | 80.99 % | 88.36 % | 91.36 % |
| 0.35 ATR | 1.17 % | 1141.095 | 53.65 % | 65.75 % | 71.05 % | 76.63 % | 85.77 % | 89.25 % |
| 0.5 ATR | 1.671 % | 1135.3071 | 40.04 % | 54.49 % | 61.26 % | 68.81 % | 80.1 % | 83.62 % |
| 0.75 ATR | 2.506 % | 1125.6607 | 23.47 % | 38.8 % | 46.84 % | 57.23 % | 70.25 % | 76.88 % |
| 1.0 ATR | 3.342 % | 1116.0143 | 12.92 % | 26.46 % | 35.97 % | 48.02 % | 61.99 % | 70.35 % |
| 1.25 ATR | 4.177 % | 1106.3678 | 7.4 % | 17.87 % | 26.19 % | 38.71 % | 53.73 % | 63.82 % |
| 1.5 ATR | 5.013 % | 1096.7214 | 3.94 % | 12.93 % | 20.45 % | 31.29 % | 45.47 % | 56.48 % |
| 2.0 ATR | 6.684 % | 1077.4285 | 1.78 % | 6.91 % | 11.96 % | 20.59 % | 33.83 % | 46.73 % |
| 2.5 ATR | 8.355 % | 1058.1357 | 0.49 % | 3.36 % | 6.23 % | 12.48 % | 24.68 % | 37.49 % |
| 3.0 ATR | 10.026 % | 1038.8428 | 0.1 % | 1.38 % | 3.85 % | 7.52 % | 16.92 % | 30.85 % |
| 4.0 ATR | 13.368 % | 1000.2571 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.46 % | 19.8 % |
| 6.0 ATR | 20.051 % | 923.0857 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.57 ATR | 0.65 ATR | 0.87 ATR | 1.04 ATR | 1.19 ATR | 1.74 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.69 ATR | 0.79 ATR | 1.08 ATR | 1.30 ATR | 1.53 ATR | 2.17 ATR | 2.76 ATR |
| **5 s.** | 0.38 ATR | 0.95 ATR | 1.08 ATR | 1.44 ATR | 1.79 ATR | 2.04 ATR | 2.75 ATR | 3.59 ATR |
| **10 s.** | 0.63 ATR | 1.36 ATR | 1.52 ATR | 2.04 ATR | 2.48 ATR | 2.80 ATR | 3.82 ATR | 4.90 ATR |
| **20 s.** | 0.82 ATR | 1.83 ATR | 2.09 ATR | 2.84 ATR | 3.53 ATR | 3.98 ATR | 5.20 ATR | 5.82 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.445–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.651–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.506 %, prix 1125.6657), p(touche) 38.8 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 53.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.792–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.342 %, prix 1116.0132), p(touche) 35.97 % (en stress 95.1 %)  ✅ optimum identifie (67.4 % des re-echantillons)
- **5 seance(s)** : plage utile 1.081–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.177 %, prix 1106.3723), p(touche) 38.71 % (en stress 98.02 %)  ✅ optimum identifie (86.8 % des re-echantillons)
- **10 seance(s)** : plage utile 1.52–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.684 %, prix 1077.4265), p(touche) 33.83 % (en stress 96.04 %)  ✅ optimum identifie (99.2 % des re-echantillons)
- **20 seance(s)** : plage utile 2.094–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.355 %, prix 1058.1331), p(touche) 37.49 % (en stress 98.0 %)  ✅ optimum identifie (99.2 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.093 | EV/share : €2.148 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 66 % | T2 44 % | T3 27 %
- Kelly (position) : f* 0.177 | ¼-Kelly 0.044 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 73.1 | bear 20.9 | side 6.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.49% → cible +1.102% / stop −2.0%, p_fill 87%, n_eff≈35.0) : P(cible|rempli) **61%** · **EV/risk +0.016** (×p_fill ; si rempli +0.04% du capital)
  - **swing** (entrée dip −1.088% → cible +2.464% / stop −3.379%, p_fill 74%, n_eff≈29.5) : P(cible|rempli) **54%** · **EV/risk -0.093** (×p_fill ; si rempli -0.42% du capital)
  - **deep** (entrée dip −1.677% → cible +3.485% / stop −5.098%, p_fill 61%, n_eff≈26.3) : P(cible|rempli) **84%** · **EV/risk +0.244** (×p_fill ; si rempli +2.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→71% · +2.0%→50% · +3.0%→32% · +5.0%→5% · +8.0%→1%
- Range intraday médian 4.1% (p90 6.82%) · excursion haute méd. +2.05% / basse méd. −1.62%
- Profil de vol intra : ouverture 2.634% vs midi 0.947% vs clôture 1.086% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.095 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.054% ; recovery-V 27%
- **σ réalisé intraday** 2.599% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 54% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1175.7525 (VA 1171.2125–1183.6975 ; dernier close 1176.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 64% · **stop −3.05%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.5 (high win-rate)
- Gaps overnight (n=159) : méd. 0.56% · baisse 30% (gap-down >1% 9% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.74%) · haut méd +0.51% · range méd 1.35%
- Excursion ouverture 15min (n=160) : bas méd −0.91% (p90 −1.98%) · haut méd +0.65% · range méd 1.73%
- Excursion ouverture 30min (n=160) : bas méd −0.94% (p90 −2.16%) · haut méd +0.81% · range méd 1.99%
- Excursion ouverture 60min (n=160) : bas méd −0.97% (p90 −2.61%) · haut méd +1.0% · range méd 2.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1173.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 67% (104/159) · gap 20% · délai 0.9min · rebond 57% (57/104) (MFE +1.14%)
   - −1.0% : fill 30min 39% · séance 61% (92/159) · gap 9% · délai 5.8min · rebond 67% (57/92) (MFE +1.32%)
   - −1.5% : fill 30min 24% · séance 47% (76/159) · gap 6% · délai 21.9min · rebond 64% (45/76) (MFE +1.42%)
   - −2.0% : fill 30min 17% · séance 41% (64/159) · gap 4% · délai 54.5min · rebond 64% (40/64) (MFE +1.51%)
   - −3.0% : fill 30min 7% · séance 21% (32/159) · gap 3% · délai 151.5min · rebond 46% (16/32) (MFE +0.93%)
   - −4.0% : fill 30min 4% · séance 14% (23/159) · gap 2% · délai 174.9min · rebond 69% (14/23) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −1.47%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.7%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=537 jambes) : jambe baissière méd −1.05% (p90 −2.47%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (34 séances) :
      · −1.0% : fill 96% (33/34) · rebond 80% (25/33)
      · −2.0% : fill 76% (28/34) · rebond 66% (19/28)
      · −3.0% : fill 40% (13/34) · rebond 60% (8/13)
      · −4.0% : fill 34% (11/34) · rebond 72% (8/11)
      · −5.0% : fill 23% (7/34) · rebond 100% (7/7)
   - **flat** (19 séances) :
      · −1.0% : fill 82% (13/19) · rebond 68% (10/13)
      · −2.0% : fill 46% (7/19) · rebond 64% (5/7)
      · −3.0% : fill 20% (3/19) · rebond 0% (0/3)
      · −4.0% : fill 10% (2/19) · rebond 62% (1/2)
      · −5.0% : fill 10% (2/19) · rebond 62% (1/2)
   - **gap-up** (106 séances) :
      · −1.0% : fill 44% (46/106) · rebond 55% (22/46)
      · −2.0% : fill 27% (29/106) · rebond 61% (16/29)
      · −3.0% : fill 14% (16/106) · rebond 49% (8/16)
      · −4.0% : fill 7% (10/106) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/106) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 60% si les 15 1res min sont vertes (75 cas) · 36% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 66% si début vert vs 28% si rouge (base 47% · écart 38 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **66%** · continue >prix actuel 40% ; creux résiduel méd -1.25% (q20 -2.93%) → **SL/trailing à −2.93%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.26% / q75 +1.88% → **scale +1.26% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **28%** (continue à baisser 47%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.29%** (au-delà de la MAE q10 -4.29%), cible rebond +1.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.22%] · haut q95 +3.66% · bas q05 -2.98%
   - 60min (n=160) : retour [-2.75% .. +3.21%] · haut q95 +4.33% · bas q05 -3.7%
   - 2h (n=160) : retour [-3.15% .. +2.99%] · haut q95 +4.36% · bas q05 -4.39%
   - 4h (n=160) : retour [-3.29% .. +3.16%] · haut q95 +4.86% · bas q05 -4.6%
   - 6h (n=160) : retour [-4.04% .. +3.25%] · haut q95 +4.9% · bas q05 -4.99%
   - session (n=160) : retour [-4.68% .. +3.67%] · haut q95 +5.03% · bas q05 -5.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 52.5  _(neutre)_
- **ADX** : 17.6  _(pas de tendance nette)_
- **MACD** : hist -5.82  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 9.7%
- **ATR** : 38.59 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.218  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 54.4  _(transition)_
- **MA** : MA20 1166.76 · MA50 1091.27 · MA200 1403.27  _(prix < MA20)_
- **Dist MA** : MA20 -1.0% · MA50 +5.8% · MA200 -17.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (920784 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
