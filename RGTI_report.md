# RGTI

**Generated** : 2026-09-04T00:31:18.176182+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.19  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.19 (+3.7% vs entrée) · entrée $14.65 · stop $14.23 · T1 $15.50 · R/R 2.02  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.121 _(réel 5 s)_ (GBM 0.247) · ¼-Kelly 0.044 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.9% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +4.2 % ≠ (strike 15.5 − spot 15.19)/spot = +2.0 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $14.57–$14.73 (mid $14.65)
- Spot actuel : $15.19 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $14.23 (stop swing_plan-based (-14.37%))
- Targets : T1 $15.50 · R/R 2.02 | T2 $15.67 · R/R 2.43 | T3 $15.84 · R/R 2.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.23


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.38 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.37 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1253).
   - exécution **1.916 pt plus bas** dans le cas TYPIQUE (médiane), 12.854 au p90, **16.843 au pire**
   - perte réelle **19.597 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 14.37 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0167 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.104 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4529** [0.38 ; 0.5273] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.4721** [0.4199 ; 0.5248] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4893** [0.4369 ; 0.5419] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (47.1 pt), swing (47.8 pt), deep (45.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 360 séances)** : VaR **-8.77 %** | CVaR **-10.77 %** | vol 6.83 %/j
   - _fenêtre arrêtée : rupture de regime a 420 seances en arriere (volatilite 14.12 % contre 6.50 % aujourd'hui, rapport 2.17)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8183** (β de hausse 1.9892, asymétrie 0.9141) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.664× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 13.2164 sur atr_grid (2.0 ATR, 13.021 %) — p(stop avant cible) 0.4899 [0.44 ; 0.54], R/R 1.317, perte reelle 17.61 % (gap inclus), CVaR 13.043 %, EV -2.6728 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0869 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 13.04 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.766 %) — p(stop avant cible) 0.6432 [0.59 ; 0.69], R/R 1.595, perte reelle 14.538 % (gap inclus), EV -3.889 % — **REFUSE**
      - refuse : p_stop_first 0.643, borne haute 0.692 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.89 %) : P(cible) 20.9 % x 23.19 % + P(rien) 14.7 % x 4.12 % ne couvrent pas P(stop) 64.3 % x 14.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.3 ATR (stop 18.134 %) — p(stop avant cible) 0.2792 [0.23 ; 0.33], R/R 0.743, perte reelle 31.213 % (gap inclus), EV -3.6784 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.14 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.68 %) : P(cible) 25.0 % x 23.19 % + P(rien) 47.1 % x -1.60 % ne couvrent pas P(stop) 27.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.69 ATR (stop 20.729 %) — p(stop avant cible) 0.2092 [0.17 ; 0.25], R/R 0.743, perte reelle 31.213 % (gap inclus), EV -2.0353 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.74 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.04 %) : P(cible) 25.6 % x 23.19 % + P(rien) 53.5 % x -2.69 % ne couvrent pas P(stop) 20.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.628 %) — p(stop avant cible) 0.9147 [0.88 ; 0.94], R/R 6.049, perte reelle 3.833 % (gap inclus), EV -1.6953 % — **REFUSE**
      - refuse : cible atteinte seulement 7.5 % du temps (< 15 %) meme a 10 seances : le R/R de 6.05 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.915, borne haute 0.941 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 7.5 % x 23.19 % + P(rien) 1.1 % x 7.50 % ne couvrent pas P(stop) 91.5 % x 3.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.255 %) — p(stop avant cible) 0.8432 [0.80 ; 0.88], R/R 3.783, perte reelle 6.13 % (gap inclus), EV -2.1034 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.843, borne haute 0.879 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 12.0 % x 23.19 % + P(rien) 3.6 % x 7.63 % ne couvrent pas P(stop) 84.3 % x 6.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.883 %) — p(stop avant cible) 0.7953 [0.75 ; 0.84], R/R 2.729, perte reelle 8.495 % (gap inclus), EV -2.976 % — **REFUSE**
      - refuse : cible atteinte seulement 14.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.795, borne haute 0.835 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.73 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.98 %) : P(cible) 14.3 % x 23.19 % + P(rien) 6.2 % x 7.59 % ne couvrent pas P(stop) 79.5 % x 8.50 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.511 %) — p(stop avant cible) 0.7332 [0.68 ; 0.78], R/R 2.024, perte reelle 11.454 % (gap inclus), EV -3.7074 % — **REFUSE**
      - refuse : p_stop_first 0.733, borne haute 0.778 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.71 %) : P(cible) 17.8 % x 23.19 % + P(rien) 8.9 % x 6.33 % ne couvrent pas P(stop) 73.3 % x 11.45 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 8.138 %) — p(stop avant cible) 0.6898 [0.64 ; 0.74], R/R 1.822, perte reelle 12.728 % (gap inclus), EV -3.6597 % — **REFUSE**
      - refuse : p_stop_first 0.690, borne haute 0.737 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.66 %) : P(cible) 19.4 % x 23.19 % + P(rien) 11.6 % x 5.31 % ne couvrent pas P(stop) 69.0 % x 12.73 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 11.394 %) — p(stop avant cible) 0.5887 [0.54 ; 0.64], R/R 1.378, perte reelle 16.825 % (gap inclus), EV -4.1716 % — **REFUSE**
      - refuse : p_stop_first 0.589, borne haute 0.640 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.17 %) : P(cible) 21.9 % x 23.19 % + P(rien) 19.3 % x 3.44 % ne couvrent pas P(stop) 58.9 % x 16.82 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 13.021 %) — p(stop avant cible) 0.4899 [0.44 ; 0.54], R/R 1.317, perte reelle 17.61 % (gap inclus), EV -2.6728 % — **REFUSE**
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.04 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.67 %) : P(cible) 22.8 % x 23.19 % + P(rien) 28.2 % x 2.34 % ne couvrent pas P(stop) 49.0 % x 17.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.3 ATR (stop 16.896 %) — p(stop avant cible) 0.3367 [0.29 ; 0.39], R/R 0.944, perte reelle 24.565 % (gap inclus), EV -2.8577 % — **REFUSE**
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.91 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.86 %) : P(cible) 24.5 % x 23.19 % + P(rien) 41.8 % x -0.65 % ne couvrent pas P(stop) 33.7 % x 24.57 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 2.69 ATR (stop 19.492 %) — p(stop avant cible) 0.249 [0.21 ; 0.30], R/R 0.743, perte reelle 31.213 % (gap inclus), EV -2.887 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.50 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.89 %) : P(cible) 25.5 % x 23.19 % + P(rien) 49.6 % x -2.07 % ne couvrent pas P(stop) 24.9 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 22.787 %) — p(stop avant cible) 0.143 [0.11 ; 0.18], R/R 0.743, perte reelle 31.213 % (gap inclus), EV -0.9045 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 25.7 % x 23.19 % + P(rien) 60.0 % x -4.00 % ne couvrent pas P(stop) 14.3 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 26.042 %) — p(stop avant cible) 0.0911 [0.06 ; 0.12], R/R 0.743, perte reelle 31.213 % (gap inclus), EV -0.0261 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.03 %) : P(cible) 26.1 % x 23.19 % + P(rien) 64.8 % x -5.00 % ne couvrent pas P(stop) 9.1 % x 31.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 29.298 %) — p(stop avant cible) 0.0698 [0.05 ; 0.10], R/R 0.743, perte reelle 31.213 % (gap inclus), EV 0.2772 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.30 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 32.553 %) — p(stop avant cible) 0.0427 [0.03 ; 0.07], R/R 0.712, perte reelle 32.553 % (gap inclus), EV 0.4538 % — **REFUSE**
      - refuse : R/R 0.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.55 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.808 %) — p(stop avant cible) 0.0264 [0.01 ; 0.05], R/R 0.648, perte reelle 35.808 % (gap inclus), EV 0.5046 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.81 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.064 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 0.594, perte reelle 39.064 % (gap inclus), EV 0.5433 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.06 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.319 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 0.548, perte reelle 42.319 % (gap inclus), EV 0.6067 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.32 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.574 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.509, perte reelle 45.574 % (gap inclus), EV 0.5986 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.57 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.83 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.475, perte reelle 48.83 % (gap inclus), EV 0.5992 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.83 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 52.085 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 0.445, perte reelle 52.085 % (gap inclus), EV 0.5879 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.08 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.195, ATR14 0.9893 (6.511 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.41 ATR = 2.669 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.326 % | 15.1455 | 92.15 % | 94.56 % | 95.66 % | 97.07 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.651 % | 15.0961 | 86.4 % | 91.23 % | 92.43 % | 94.94 % | 95.83 % | 97.43 % |
| 0.15 ATR | 0.977 % | 15.0466 | 80.97 % | 87.5 % | 89.1 % | 92.01 % | 93.9 % | 96.1 % |
| 0.2 ATR | 1.302 % | 14.9971 | 74.52 % | 82.96 % | 85.67 % | 88.88 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.628 % | 14.9477 | 68.38 % | 78.73 % | 81.84 % | 85.84 % | 88.82 % | 92.51 % |
| 0.35 ATR | 2.279 % | 14.8487 | 55.89 % | 68.55 % | 74.07 % | 79.68 % | 84.45 % | 89.63 % |
| 0.5 ATR | 3.255 % | 14.7004 | 41.09 % | 56.96 % | 64.98 % | 71.89 % | 79.27 % | 85.52 % |
| 0.75 ATR | 4.883 % | 14.453 | 21.75 % | 38.91 % | 49.55 % | 59.15 % | 70.93 % | 79.26 % |
| 1.0 ATR | 6.511 % | 14.2057 | 9.57 % | 23.69 % | 33.6 % | 46.41 % | 61.89 % | 73.0 % |
| 1.25 ATR | 8.138 % | 13.9584 | 4.03 % | 14.52 % | 23.61 % | 37.01 % | 52.85 % | 65.09 % |
| 1.5 ATR | 9.766 % | 13.7111 | 1.71 % | 7.16 % | 13.72 % | 25.68 % | 43.09 % | 56.78 % |
| 2.0 ATR | 13.021 % | 13.2164 | 0.4 % | 1.71 % | 3.94 % | 10.72 % | 25.61 % | 40.86 % |
| 2.5 ATR | 16.277 % | 12.7218 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.43 % | 28.44 % |
| 3.0 ATR | 19.532 % | 12.2271 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.11 % | 17.15 % |
| 4.0 ATR | 26.042 % | 11.2379 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 4.93 % |
| 6.0 ATR | 39.064 % | 9.2593 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 1.03 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.98 ATR | 1.10 ATR | 1.40 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.74 ATR | 0.82 ATR | 1.01 ATR | 1.22 ATR | 1.34 ATR | 1.69 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.34 ATR | 1.52 ATR | 1.69 ATR | 2.06 ATR | 2.46 ATR |
| **10 s.** | 0.63 ATR | 1.32 ATR | 1.45 ATR | 1.79 ATR | 2.03 ATR | 2.25 ATR | 2.80 ATR | 3.41 ATR |
| **20 s.** | 0.92 ATR | 1.71 ATR | 1.87 ATR | 2.32 ATR | 2.65 ATR | 2.87 ATR | 3.58 ATR | 3.99 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.46–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.255 %, prix 14.7004), p(touche) 41.09 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (67.5 % des re-echantillons)
- **2 seance(s)** : plage utile 0.666–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.883 %, prix 14.453), p(touche) 38.91 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 43.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.821–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.511 %, prix 14.2057), p(touche) 33.6 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.037–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.138 %, prix 13.9584), p(touche) 37.01 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.766 %, prix 13.7111), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.87–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.021 %, prix 13.2165), p(touche) 40.86 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.247 | EV/share : $0.105 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 37 % | T3 37 %
- Kelly (position) : f* 0.178 | ¼-Kelly 0.044 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 21.1 | side 73.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.573% → cible +5.801% / stop −2.901%, p_fill 35%, n_eff≈14.6) : P(cible|rempli) **3%** · **EV/risk -0.121** (×p_fill ; si rempli -1.01% du capital)
  - **swing** (entrée dip −7.859% → cible +6.066% / stop −7.066%, p_fill 17%, n_eff≈10.9) : P(cible|rempli) **74%** · **EV/risk +0.074** (×p_fill ; si rempli +3.02% du capital)
  - **deep** (entrée dip −12.143% → cible +8.579% / stop −11.117%, p_fill 22%, n_eff≈12.0) : P(cible|rempli) **75%** · **EV/risk +0.083** (×p_fill ; si rempli +4.21% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→78% · +2.0%→70% · +3.0%→52% · +5.0%→39% · +8.0%→12%
- Range intraday médian 7.47% (p90 11.35%) · excursion haute méd. +3.41% / basse méd. −2.61%
- Profil de vol intra : ouverture 5.319% vs midi 1.534% vs clôture 1.745% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 25% · trend ↑0%/↓0% ; spike-down 70% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; mean-reverting — autocorr -0.049)_ ; drift intra méd. -0.087% ; recovery-V 31%
- **σ réalisé intraday** 4.107% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 36% / bas 49% / whipsaw 4%
- POC intraday (dernière séance, temps-au-prix) : 14.9997 (VA 14.8963–14.9997 ; dernier close 14.9977)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 45% · rebond 74% · **stop −5.84%** sous le fill (sous le bruit) · cible +1.98% · R/R 0.34 (high win-rate)
- Gaps overnight (n=159) : méd. -0.58% · baisse 61% (gap-down >1% 42% · >2% 27%)
- Excursion ouverture 5min (n=160) : bas méd −1.17% (p90 −2.88%) · haut méd +1.28% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.73%) · haut méd +1.8% · range méd 3.6%
- Excursion ouverture 30min (n=160) : bas méd −1.73% (p90 −4.53%) · haut méd +2.09% · range méd 4.41%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −5.53%) · haut méd +2.24% · range méd 5.23%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 14.99 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 82% (133/159) · gap 51% · délai 0.0min · rebond 62% (83/133) (MFE +1.96%)
   - −1.0% : fill 30min 66% · séance 73% (124/159) · gap 42% · délai 0.0min · rebond 62% (77/124) (MFE +1.61%)
   - −1.5% : fill 30min 61% · séance 68% (118/159) · gap 34% · délai 0.0min · rebond 63% (76/118) (MFE +1.9%)
   - −2.0% : fill 30min 54% · séance 62% (109/159) · gap 27% · délai 0.0min · rebond 63% (72/109) (MFE +1.83%)
   - −3.0% : fill 30min 46% · séance 56% (98/159) · gap 11% · délai 1.2min · rebond 64% (69/98) (MFE +1.9%)
   - −4.0% : fill 30min 35% · séance 45% (77/159) · gap 6% · délai 6.3min · rebond 74% (55/77) (MFE +1.98%)
   - −5.0% : fill 30min 19% · séance 38% (67/159) · gap 2% · délai 27.1min · rebond 57% (45/67) (MFE +1.27%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.32%) → stop au-delà de −1.66% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −2.78%) → stop au-delà de −2.03% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −2.9%) → stop au-delà de −2.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1146 jambes) : jambe baissière méd −1.28% (p90 −3.1%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (86 séances) :
      · −1.0% : fill 93% (83/86) · rebond 56% (47/83)
      · −2.0% : fill 84% (78/86) · rebond 60% (49/78)
      · −3.0% : fill 81% (74/86) · rebond 57% (49/74)
      · −4.0% : fill 69% (60/86) · rebond 72% (42/60)
      · −5.0% : fill 59% (53/86) · rebond 54% (35/53)
   - **flat** (15 séances) :
      · −1.0% : fill 96% (14/15) · rebond 94% (12/14)
      · −2.0% : fill 74% (12/15) · rebond 85% (10/12)
      · −3.0% : fill 50% (7/15) · rebond 90% (5/7)
      · −4.0% : fill 34% (6/15) · rebond 85% (4/6)
      · −5.0% : fill 21% (5/15) · rebond 87% (3/5)
   - **gap-up** (58 séances) :
      · −1.0% : fill 36% (27/58) · rebond 67% (18/27)
      · −2.0% : fill 25% (19/58) · rebond 64% (13/19)
      · −3.0% : fill 21% (17/58) · rebond 90% (15/17)
      · −4.0% : fill 13% (11/58) · rebond 83% (9/11)
      · −5.0% : fill 11% (9/58) · rebond 67% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 73% si les 15 1res min sont vertes (81 cas) · 27% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 94% si début vert vs 9% si rouge (base 51% · écart 85 pts) ; prédictivité sature ensuite (plafond brut 91min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **94%** · continue >prix actuel 56% ; creux résiduel méd -1.81% (q20 -2.87%) → **SL/trailing à −2.87%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.17% / q75 +4.14% → **scale +2.17% / runner +4.14%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **9%** (continue à baisser 67%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.52%** (au-delà de la MAE q10 -5.52%), cible rebond +1.1% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.0% .. +4.82%] · haut q95 +6.36% · bas q05 -6.02%
   - 60min (n=160) : retour [-5.32% .. +6.14%] · haut q95 +6.62% · bas q05 -6.62%
   - 2h (n=160) : retour [-6.27% .. +6.62%] · haut q95 +8.85% · bas q05 -7.34%
   - 4h (n=160) : retour [-6.49% .. +7.81%] · haut q95 +9.18% · bas q05 -7.79%
   - 6h (n=160) : retour [-7.19% .. +8.64%] · haut q95 +9.97% · bas q05 -8.49%
   - session (n=160) : retour [-7.1% .. +9.03%] · haut q95 +10.34% · bas q05 -8.6%


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

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.3  _(momentum baissier)_
- **ADX** : 15.2  _(pas de tendance nette)_
- **MACD** : hist -0.253  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 31.0%
- **ATR** : 0.99 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.017  _(neutre)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 43.8  _(transition)_
- **MA** : MA20 16.94 · MA50 16.49 · MA200 19.34  _(prix < MA20)_
- **Dist MA** : MA20 -10.3% · MA50 -7.9% · MA200 -21.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763582 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
