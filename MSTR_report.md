# MSTR

**Generated** : 2026-09-16T00:32:04.547557+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $129.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot $129.64 (+5.5% vs entrée) · entrée $122.91 · stop $113.35 · T1 $136.25 · R/R 1.4  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk 0.078 _(réel 5 s)_ (GBM -0.052) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -10.9 % ≠ (strike 122.0 − spot 129.64)/spot = -5.9 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $120.89–$124.92 (mid $122.91)
- Spot actuel : $129.64 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : $113.35 (stop swing_plan-based (-12.56%))
- Targets : T1 $136.25 · R/R 1.4 | T2 $152.31 · R/R 3.08 | T3 $153.03 · R/R 3.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $113.35


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.62 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.56 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **14.018 pt plus bas** dans le cas TYPIQUE (médiane), 14.653 au p90, **14.812 au pire**
   - perte réelle **22.94 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 12.56 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0249 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.493 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2816** [0.2186 ; 0.3518] _(largeur 13.3 pt, n_eff 173.1)_
   - swing : **0.3798** [0.3298 ; 0.4318] _(largeur 10.2 pt, n_eff 345.7)_
   - deep : **0.3013** [0.2547 ; 0.3512] _(largeur 9.6 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 17.8 observations effectives », dont la borne haute a 95 % vaut environ 16.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (29.5 pt), swing (50.7 pt), deep (41.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.66 %** | CVaR **-10.34 %** | vol 5.47 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.66 % contre 5.13 % aujourd'hui, rapport 1.69)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3414** (β de hausse 1.8358, asymétrie 1.2754) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 116.7069 sur swing_based (1.06 ATR, 9.976 %) — p(stop avant cible) 0.4418 [0.39 ; 0.49], R/R 1.048, perte reelle 17.215 % (gap inclus), CVaR 10.011 %, EV -3.2286 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 1.06 ATR (stop 9.976 %) — p(stop avant cible) 0.4418 [0.39 ; 0.49], R/R 1.048, perte reelle 17.215 % (gap inclus), EV -3.2286 % — **REFUSE**
      - refuse : R/R 1.05 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.23 %) : P(cible) 20.0 % x 18.04 % + P(rien) 35.8 % x 2.13 % ne couvrent pas P(stop) 44.2 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.39 ATR (stop 12.343 %) — p(stop avant cible) 0.353 [0.30 ; 0.40], R/R 0.787, perte reelle 22.94 % (gap inclus), EV -3.9583 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.37 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.96 %) : P(cible) 20.4 % x 18.04 % + P(rien) 44.3 % x 1.04 % ne couvrent pas P(stop) 35.3 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 2.67 ATR (stop 21.777 %) — p(stop avant cible) 0.1411 [0.11 ; 0.18], R/R 0.669, perte reelle 26.975 % (gap inclus), EV -1.6813 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.79 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.68 %) : P(cible) 20.8 % x 18.04 % + P(rien) 65.1 % x -2.49 % ne couvrent pas P(stop) 14.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.23 ATR (stop 33.317 %) — p(stop avant cible) 0.0275 [0.01 ; 0.05], R/R 0.542, perte reelle 33.317 % (gap inclus), EV -0.94 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.94 %) : P(cible) 20.8 % x 18.04 % + P(rien) 76.5 % x -4.94 % ne couvrent pas P(stop) 2.8 % x 33.32 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.843 %) — p(stop avant cible) 0.9019 [0.87 ; 0.93], R/R 4.778, perte reelle 3.776 % (gap inclus), EV -2.0207 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.902, borne haute 0.930 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.02 %) : P(cible) 6.5 % x 18.04 % + P(rien) 3.3 % x 6.37 % ne couvrent pas P(stop) 90.2 % x 3.78 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.686 %) — p(stop avant cible) 0.7811 [0.74 ; 0.82], R/R 2.803, perte reelle 6.437 % (gap inclus), EV -2.1012 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.781, borne haute 0.822 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.10 %) : P(cible) 14.1 % x 18.04 % + P(rien) 7.8 % x 4.93 % ne couvrent pas P(stop) 78.1 % x 6.44 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.529 %) — p(stop avant cible) 0.6642 [0.61 ; 0.71], R/R 2.125, perte reelle 8.49 % (gap inclus), EV -1.9044 % — **REFUSE**
      - refuse : p_stop_first 0.664, borne haute 0.713 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 16.7 % x 18.04 % + P(rien) 16.9 % x 4.31 % ne couvrent pas P(stop) 66.4 % x 8.49 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 14.743 %) — p(stop avant cible) 0.2748 [0.23 ; 0.32], R/R 0.787, perte reelle 22.94 % (gap inclus), EV -2.7431 % — **REFUSE**
      - refuse : R/R 0.79 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.76 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.74 %) : P(cible) 20.6 % x 18.04 % + P(rien) 51.9 % x -0.30 % ne couvrent pas P(stop) 27.5 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 16.586 %) — p(stop avant cible) 0.2235 [0.18 ; 0.27], R/R 0.669, perte reelle 26.975 % (gap inclus), EV -2.9833 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.98 %) : P(cible) 20.7 % x 18.04 % + P(rien) 56.9 % x -1.22 % ne couvrent pas P(stop) 22.4 % x 26.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.5 ATR (stop 25.8 %) — p(stop avant cible) 0.084 [0.06 ; 0.12], R/R 0.669, perte reelle 26.975 % (gap inclus), EV -1.0599 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.06 %) : P(cible) 20.8 % x 18.04 % + P(rien) 70.8 % x -3.60 % ne couvrent pas P(stop) 8.4 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 36.858 %) — p(stop avant cible) 0.0063 [0.00 ; 0.02], R/R 0.49, perte reelle 36.858 % (gap inclus), EV -0.7806 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.86 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.78 %) : P(cible) 20.8 % x 18.04 % + P(rien) 78.6 % x -5.47 % ne couvrent pas P(stop) 0.6 % x 36.86 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 40.543 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.445, perte reelle 40.543 % (gap inclus), EV -0.7413 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.74 %) : P(cible) 20.8 % x 18.04 % + P(rien) 79.1 % x -5.63 % ne couvrent pas P(stop) 0.1 % x 40.54 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 44.229 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.408, perte reelle 44.229 % (gap inclus), EV -0.7277 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.23 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 20.8 % x 18.04 % + P(rien) 79.2 % x -5.65 % ne couvrent pas P(stop) 0.0 % x 44.23 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 47.915 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.377, perte reelle 47.915 % (gap inclus), EV -0.7296 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.92 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 20.8 % x 18.04 % + P(rien) 79.2 % x -5.65 % ne couvrent pas P(stop) 0.0 % x 47.91 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 51.601 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.35, perte reelle 51.601 % (gap inclus), EV -0.7312 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 20.8 % x 18.04 % + P(rien) 79.2 % x -5.66 % ne couvrent pas P(stop) 0.0 % x 51.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 55.286 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.326, perte reelle 55.286 % (gap inclus), EV -0.7316 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 55.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 20.8 % x 18.04 % + P(rien) 79.2 % x -5.66 % ne couvrent pas P(stop) 0.0 % x 55.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 58.972 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.306, perte reelle 58.972 % (gap inclus), EV -0.7328 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 58.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 20.8 % x 18.04 % + P(rien) 79.2 % x -5.66 % ne couvrent pas P(stop) 0.0 % x 58.97 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 129.64, ATR14 9.5564 (7.372 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 2.904 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.369 % | 129.1622 | 94.16 % | 96.67 % | 97.07 % | 97.78 % | 98.17 % | 98.77 % |
| 0.1 ATR | 0.737 % | 128.6844 | 88.12 % | 92.04 % | 93.44 % | 94.84 % | 96.65 % | 97.43 % |
| 0.15 ATR | 1.106 % | 128.2065 | 81.17 % | 87.0 % | 89.61 % | 91.71 % | 94.11 % | 95.69 % |
| 0.2 ATR | 1.474 % | 127.7287 | 73.51 % | 81.55 % | 84.76 % | 88.07 % | 91.36 % | 93.74 % |
| 0.25 ATR | 1.843 % | 127.2509 | 67.67 % | 77.72 % | 81.94 % | 86.05 % | 89.13 % | 92.2 % |
| 0.35 ATR | 2.58 % | 126.2952 | 54.98 % | 68.65 % | 75.18 % | 80.79 % | 85.67 % | 89.63 % |
| 0.5 ATR | 3.686 % | 124.8618 | 38.17 % | 55.14 % | 63.27 % | 71.18 % | 78.46 % | 84.8 % |
| 0.75 ATR | 5.529 % | 122.4727 | 19.44 % | 37.6 % | 47.02 % | 57.94 % | 67.89 % | 77.31 % |
| 1.0 ATR | 7.372 % | 120.0836 | 9.37 % | 25.3 % | 34.91 % | 46.51 % | 58.94 % | 70.53 % |
| 1.25 ATR | 9.214 % | 117.6945 | 4.13 % | 14.62 % | 25.13 % | 36.0 % | 49.9 % | 62.94 % |
| 1.5 ATR | 11.057 % | 115.3054 | 2.11 % | 8.77 % | 17.46 % | 29.02 % | 43.09 % | 57.08 % |
| 2.0 ATR | 14.743 % | 110.5271 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.3 % | 47.23 % |
| 2.5 ATR | 18.429 % | 105.7489 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 22.115 % | 100.9707 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 29.486 % | 91.4143 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 44.229 % | 72.3014 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.39 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.01 ATR | 1.12 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.70 ATR | 0.79 ATR | 1.05 ATR | 1.25 ATR | 1.42 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.92 ATR | 1.04 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.439–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.686 %, prix 124.8615), p(touche) 38.17 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.645–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.529 %, prix 122.4722), p(touche) 37.6 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.792–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (7.372 %, prix 120.0829), p(touche) 34.91 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.036–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (9.214 %, prix 117.695), p(touche) 36.0 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.43–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (11.057 %, prix 115.3057), p(touche) 43.09 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 33.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.116–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (18.429 %, prix 105.7486), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.052 | EV/share : $-0.497 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 5 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.5 | bear 45.6 | side 34.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 259.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.363% → cible +6.179% / stop −3.5%, p_fill 39%, n_eff≈19.0) : P(cible|rempli) **2%** · **EV/risk -0.039** (×p_fill ; si rempli -0.34% du capital)
  - **swing** (entrée dip −5.188% → cible +10.855% / stop −7.775%, p_fill 21%, n_eff≈12.4) : P(cible|rempli) **28%** · **EV/risk +0.078** (×p_fill ; si rempli +2.90% du capital)
  - **deep** (entrée dip −8.025% → cible +27.735% / stop −13.868%, p_fill 16%, n_eff≈17.8) : P(cible|rempli) **0%** · **EV/risk -0.037** (×p_fill ; si rempli -3.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→59% · +3.0%→44% · +5.0%→18% · +8.0%→10%
- Range intraday médian 5.55% (p90 10.31%) · excursion haute méd. +2.54% / basse méd. −2.28%
- Profil de vol intra : ouverture 3.455% vs midi 1.19% vs clôture 1.377% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑2%/↓0% ; spike-down 70% · recovery-V 33%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; neutre — autocorr -0.013)_ ; drift intra méd. 1.293% ; recovery-V 29%
- **σ réalisé intraday** 3.641% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 80% / bas 52% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 142.0446 (VA 141.0741–144.3091 ; dernier close 142.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 75% · **stop −4.03%** sous le fill (sous le bruit) · cible +1.96% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 53% (gap-down >1% 43% · >2% 29%)
- Excursion ouverture 5min (n=160) : bas méd −0.9% (p90 −2.0%) · haut méd +0.76% · range méd 1.83%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.91%) · haut méd +1.21% · range méd 2.57%
- Excursion ouverture 30min (n=160) : bas méd −1.28% (p90 −3.23%) · haut méd +1.43% · range méd 3.13%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −3.57%) · haut méd +1.82% · range méd 3.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 142.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 74% (121/159) · gap 46% · délai 0.0min · rebond 46% (58/121) (MFE +0.56%)
   - −1.0% : fill 30min 60% · séance 69% (116/159) · gap 43% · délai 0.0min · rebond 50% (63/116) (MFE +1.01%)
   - −1.5% : fill 30min 53% · séance 64% (109/159) · gap 34% · délai 0.0min · rebond 59% (64/109) (MFE +1.35%)
   - −2.0% : fill 30min 48% · séance 58% (99/159) · gap 29% · délai 0.0min · rebond 60% (60/99) (MFE +1.43%)
   - −3.0% : fill 30min 32% · séance 48% (80/159) · gap 15% · délai 1.2min · rebond 58% (48/80) (MFE +1.67%)
   - −4.0% : fill 30min 21% · séance 38% (66/159) · gap 6% · délai 17.9min · rebond 71% (45/66) (MFE +1.9%)
   - −5.0% : fill 30min 15% · séance 28% (48/159) · gap 5% · délai 21.4min · rebond 75% (35/48) (MFE +1.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.8% (p90 −2.45%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.43%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.93% (p90 −2.39%) → stop au-delà de −2.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=964 jambes) : jambe baissière méd −1.1% (p90 −2.68%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (79 séances) :
      · −1.0% : fill 100% (79/79) · rebond 42% (36/79)
      · −2.0% : fill 93% (73/79) · rebond 60% (42/73)
      · −3.0% : fill 81% (65/79) · rebond 60% (39/65)
      · −4.0% : fill 67% (55/79) · rebond 73% (38/55)
      · −5.0% : fill 50% (42/79) · rebond 78% (32/42)
   - **flat** (17 séances) :
      · −1.0% : fill 70% (13/17) · rebond 80% (11/13)
      · −2.0% : fill 45% (9/17) · rebond 60% (6/9)
      · −3.0% : fill 28% (5/17) · rebond 35% (2/5)
      · −4.0% : fill 12% (3/17) · rebond 51% (2/3)
      · −5.0% : fill 9% (2/17) · rebond 0% (0/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 30% (24/63) · rebond 63% (16/24)
      · −2.0% : fill 15% (17/63) · rebond 66% (12/17)
      · −3.0% : fill 10% (10/63) · rebond 57% (7/10)
      · −4.0% : fill 9% (8/63) · rebond 68% (5/8)
      · −5.0% : fill 4% (4/63) · rebond 92% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 55% si les 15 1res min sont vertes (85 cas) · 38% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:33** → P(séance verte=clôture>ouverture) 81% si début vert vs 15% si rouge (base 48% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **81%** · continue >prix actuel 47% ; creux résiduel méd -1.39% (q20 -2.95%) → **SL/trailing à −2.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.83% / q75 +2.83% → **scale +1.83% / runner +2.83%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **15%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.74%** (au-delà de la MAE q10 -4.74%), cible rebond +1.49% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.29% .. +3.69%] · haut q95 +3.94% · bas q05 -3.65%
   - 60min (n=160) : retour [-4.26% .. +5.6%] · haut q95 +5.86% · bas q05 -4.96%
   - 2h (n=160) : retour [-4.29% .. +8.45%] · haut q95 +8.77% · bas q05 -5.05%
   - 4h (n=160) : retour [-5.44% .. +9.36%] · haut q95 +10.32% · bas q05 -6.45%
   - 6h (n=160) : retour [-5.5% .. +8.47%] · haut q95 +10.93% · bas q05 -7.06%
   - session (n=160) : retour [-5.0% .. +8.29%] · haut q95 +10.93% · bas q05 -7.09%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.9% des séances sont trend-up (mild 0.6% / strong 6.2%) · base = 11 séances trend-up (n_eff 6.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **38%**. Lecture précoce 30 min : signature présente → 23% vs absente 1% (base 7%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.83% (p75 1.54% / p90 2.99%) · ~3.89 replis/séance, durée méd 35.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 19.22 min, n=40)
   - −1.0% → **61%** (reprise méd 35.89 min, n=19)
   - −1.5% → **46%** (reprise méd 37.49 min, n=15)
   - −2.0% → **20%** (reprise méd 89.44 min, n=9)
   - −3.0% → **41%** (reprise méd 89.44 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.99%** (p90, défaut prudent ; serré/agressif −1.54%) ; extension open→close méd +8.34% (q75 +10.86% / q95 +15.58%), MFE méd +10.26% / q90 +13.74%
   - Échelle scale-out : +10.26% (33%) / +13.11% (33%) / +13.74% (34%)
- **DÉSARMER** : repli > **−2.99%** depuis le plus-haut = décay → P(retournement) **59%** (préavis méd 221.98 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +13.74% : P(retournement après) 0% (mèche méd 0.76%)
- **CONTEXTE** : la dernière heure tient les gains 80% du temps (retour médian dernière heure +0.51%)


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-16 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 51.5  _(neutre)_
- **ADX** : 39.3  _(tendance etablie)_
- **MACD** : hist -0.553  _(bearish_recent)_
- **BB** : %B 0.56 · largeur 39.6%
- **ATR** : 9.56 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.177  _(accumulation)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 65.0  _(marche en range (choppy))_
- **MA** : MA20 126.49 · MA50 108.27 · MA200 137.6  _(prix > MA20)_
- **Dist MA** : MA20 +2.5% · MA50 +19.7% · MA200 -5.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (759298 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
