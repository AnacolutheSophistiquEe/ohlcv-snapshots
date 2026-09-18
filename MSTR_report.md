# MSTR

**Generated** : 2026-09-18T00:32:48.783998+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $132.28  

> 🟡 **WAIT-FOR-DIP** — spot +2.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $132.28 (+2.9% vs entrée) · entrée $128.56 · stop $124.06 · T1 $132.95 · R/R 0.98  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk 0.055 _(réel 5 s)_ (GBM 0.018) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -4.9 % ≠ (strike 120.0 − spot 132.28)/spot = -9.3 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 145 % hors [0,100] (R² max 0.80). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $127.69–$129.43 (mid $128.56)
- Spot actuel : $132.28 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : $124.06 (stop swing_plan-based (-12.97%))
- Targets : T1 $132.95 · R/R 0.98 | T2 $136.25 · R/R 1.71 | T3 $141.52 · R/R 2.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $124.06


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=10.54 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.97 %)** : le gap seul le franchit 0.239 % des séances (3 fois sur 1253).
   - exécution **13.608 pt plus bas** dans le cas TYPIQUE (médiane), 14.243 au p90, **14.402 au pire**
   - perte réelle **22.94 %** en moyenne _(tirée par la queue)_, jusqu'à **27.372 %** — au lieu des 12.97 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0239 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.43 % | p01 -7.775 % | pire -27.372 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2901** [0.2264 ; 0.3608] _(largeur 13.4 pt, n_eff 173.1)_
   - swing : **0.4372** [0.3856 ; 0.4898] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.303** [0.2564 ; 0.3529] _(largeur 9.7 pt, n_eff 345.7)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_target_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 14.3 observations effectives », dont la borne haute a 95 % vaut environ 21.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.3 pt), swing (45.2 pt), deep (47.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-7.66 %** | CVaR **-10.34 %** | vol 5.47 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 8.72 % contre 5.13 % aujourd'hui, rapport 1.70)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.99 % vs -17.67 % si l'on extrapolait par √5 _(rapport 0.962 ; < 1 = le √5 surestime)_
- **β de baisse : 2.3389** (β de hausse 1.8261, asymétrie 1.2808) vs IWM — 603 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 118.8261 sur atr_based (1.5 ATR, 10.171 %) — p(stop avant cible) 0.4113 [0.36 ; 0.46], R/R 0.869, perte reelle 17.215 % (gap inclus), CVaR 10.205 %, EV -2.7494 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.8 % de la queue et il ne reste que -887.74 EUR a partager. Prix du risque -0.635 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.171 %) — p(stop avant cible) 0.4113 [0.36 ; 0.46], R/R 0.869, perte reelle 17.215 % (gap inclus), EV -2.7494 % — **REFUSE**
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.75 %) : P(cible) 26.3 % x 14.95 % + P(rien) 32.6 % x 1.24 % ne couvrent pas P(stop) 41.1 % x 17.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.42 ATR (stop 13.088 %) — p(stop avant cible) 0.321 [0.27 ; 0.37], R/R 0.652, perte reelle 22.94 % (gap inclus), EV -3.3822 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.38 %) : P(cible) 26.5 % x 14.95 % + P(rien) 41.3 % x 0.03 % ne couvrent pas P(stop) 32.1 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.77 ATR (stop 15.497 %) — p(stop avant cible) 0.2511 [0.21 ; 0.30], R/R 0.554, perte reelle 26.975 % (gap inclus), EV -3.253 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.52 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.25 %) : P(cible) 27.2 % x 14.95 % + P(rien) 47.7 % x -1.15 % ne couvrent pas P(stop) 25.1 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.13 ATR (stop 24.742 %) — p(stop avant cible) 0.0893 [0.06 ; 0.12], R/R 0.554, perte reelle 26.975 % (gap inclus), EV -0.9464 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.95 %) : P(cible) 27.3 % x 14.95 % + P(rien) 63.7 % x -4.12 % ne couvrent pas P(stop) 8.9 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 4.8 ATR (stop 36.052 %) — p(stop avant cible) 0.0139 [0.01 ; 0.03], R/R 0.415, perte reelle 36.052 % (gap inclus), EV -0.5791 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.05 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 27.4 % x 14.95 % + P(rien) 71.2 % x -5.86 % ne couvrent pas P(stop) 1.4 % x 36.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.25 ATR (stop 1.695 %) — p(stop avant cible) 0.9151 [0.88 ; 0.94], R/R 4.138, perte reelle 3.614 % (gap inclus), EV -2.2227 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.915, borne haute 0.941 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 6.6 % x 14.95 % + P(rien) 1.9 % x 4.92 % ne couvrent pas P(stop) 91.5 % x 3.61 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 3.39 %) — p(stop avant cible) 0.7839 [0.74 ; 0.82], R/R 2.52, perte reelle 5.933 % (gap inclus), EV -1.991 % — **REFUSE**
      - refuse : p_stop_first 0.784, borne haute 0.825 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.99 %) : P(cible) 16.5 % x 14.95 % + P(rien) 5.1 % x 3.78 % ne couvrent pas P(stop) 78.4 % x 5.93 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 5.085 %) — p(stop avant cible) 0.6766 [0.63 ; 0.72], R/R 1.847, perte reelle 8.098 % (gap inclus), EV -1.8984 % — **REFUSE**
      - refuse : p_stop_first 0.677, borne haute 0.724 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.90 %) : P(cible) 20.8 % x 14.95 % + P(rien) 11.5 % x 4.05 % ne couvrent pas P(stop) 67.7 % x 8.10 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.781 %) — p(stop avant cible) 0.5586 [0.51 ; 0.61], R/R 1.466, perte reelle 10.199 % (gap inclus), EV -1.5951 % — **REFUSE**
      - refuse : p_stop_first 0.559, borne haute 0.610 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.60 %) : P(cible) 24.2 % x 14.95 % + P(rien) 20.0 % x 2.45 % ne couvrent pas P(stop) 55.9 % x 10.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.42 ATR (stop 11.63 %) — p(stop avant cible) 0.3598 [0.31 ; 0.41], R/R 0.742, perte reelle 20.144 % (gap inclus), EV -2.9924 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.99 %) : P(cible) 26.5 % x 14.95 % + P(rien) 37.5 % x 0.79 % ne couvrent pas P(stop) 36.0 % x 20.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 1.77 ATR (stop 14.039 %) — p(stop avant cible) 0.285 [0.24 ; 0.33], R/R 0.652, perte reelle 22.94 % (gap inclus), EV -2.6871 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.69 %) : P(cible) 27.1 % x 14.95 % + P(rien) 44.4 % x -0.45 % ne couvrent pas P(stop) 28.5 % x 22.94 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 16.951 %) — p(stop avant cible) 0.2046 [0.16 ; 0.25], R/R 0.554, perte reelle 26.975 % (gap inclus), EV -2.5342 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.97 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.53 %) : P(cible) 27.3 % x 14.95 % + P(rien) 52.3 % x -2.09 % ne couvrent pas P(stop) 20.5 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.75 ATR (stop 18.646 %) — p(stop avant cible) 0.1783 [0.14 ; 0.22], R/R 0.554, perte reelle 26.975 % (gap inclus), EV -2.1163 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.66 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.12 %) : P(cible) 27.3 % x 14.95 % + P(rien) 54.9 % x -2.53 % ne couvrent pas P(stop) 17.8 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 3.13 ATR (stop 23.285 %) — p(stop avant cible) 0.1146 [0.08 ; 0.15], R/R 0.554, perte reelle 26.975 % (gap inclus), EV -1.1259 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.13 %) : P(cible) 27.3 % x 14.95 % + P(rien) 61.2 % x -3.47 % ne couvrent pas P(stop) 11.5 % x 26.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 27.122 %) — p(stop avant cible) 0.0666 [0.04 ; 0.10], R/R 0.546, perte reelle 27.372 % (gap inclus), EV -0.7347 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.73 %) : P(cible) 27.4 % x 14.95 % + P(rien) 66.0 % x -4.55 % ne couvrent pas P(stop) 6.7 % x 27.37 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 30.512 %) — p(stop avant cible) 0.0362 [0.02 ; 0.06], R/R 0.49, perte reelle 30.512 % (gap inclus), EV -0.6401 % — **REFUSE**
      - refuse : R/R 0.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 27.4 % x 14.95 % + P(rien) 69.0 % x -5.26 % ne couvrent pas P(stop) 3.6 % x 30.51 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 grid_snapped a 4.8 ATR (stop 34.594 %) — p(stop avant cible) 0.0211 [0.01 ; 0.04], R/R 0.432, perte reelle 34.594 % (gap inclus), EV -0.6576 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.59 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.66 %) : P(cible) 27.4 % x 14.95 % + P(rien) 70.5 % x -5.71 % ne couvrent pas P(stop) 2.1 % x 34.59 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 37.293 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 0.401, perte reelle 37.293 % (gap inclus), EV -0.5188 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 27.4 % x 14.95 % + P(rien) 72.0 % x -6.09 % ne couvrent pas P(stop) 0.6 % x 37.29 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 40.683 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.368, perte reelle 40.683 % (gap inclus), EV -0.4782 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.68 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.48 %) : P(cible) 27.4 % x 14.95 % + P(rien) 72.5 % x -6.25 % ne couvrent pas P(stop) 0.1 % x 40.68 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 44.073 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.339, perte reelle 44.073 % (gap inclus), EV -0.4643 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.46 %) : P(cible) 27.4 % x 14.95 % + P(rien) 72.6 % x -6.27 % ne couvrent pas P(stop) 0.0 % x 44.07 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.0 ATR (stop 47.464 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.315, perte reelle 47.464 % (gap inclus), EV -0.4661 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.46 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 27.4 % x 14.95 % + P(rien) 72.6 % x -6.28 % ne couvrent pas P(stop) 0.0 % x 47.46 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 7.5 ATR (stop 50.854 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.294, perte reelle 50.854 % (gap inclus), EV -0.4671 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 50.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 27.4 % x 14.95 % + P(rien) 72.6 % x -6.28 % ne couvrent pas P(stop) 0.0 % x 50.85 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 8.0 ATR (stop 54.244 %) — p(stop avant cible) 0.0001 [0.00 ; 0.01], R/R 0.276, perte reelle 54.244 % (gap inclus), EV -0.4675 % — **REFUSE**
      - refuse : R/R 0.28 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 54.24 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.47 %) : P(cible) 27.4 % x 14.95 % + P(rien) 72.6 % x -6.28 % ne couvrent pas P(stop) 0.0 % x 54.24 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 132.28, ATR14 8.9693 (6.781 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.395 ATR = 2.678 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.339 % | 131.8315 | 94.26 % | 96.67 % | 97.07 % | 97.78 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.678 % | 131.3831 | 88.22 % | 92.04 % | 93.44 % | 94.84 % | 96.65 % | 97.33 % |
| 0.15 ATR | 1.017 % | 130.9346 | 81.27 % | 87.1 % | 89.71 % | 91.81 % | 94.21 % | 95.59 % |
| 0.2 ATR | 1.356 % | 130.4861 | 73.62 % | 81.65 % | 84.86 % | 88.17 % | 91.46 % | 93.63 % |
| 0.25 ATR | 1.695 % | 130.0377 | 67.77 % | 77.82 % | 82.04 % | 86.15 % | 89.13 % | 92.09 % |
| 0.35 ATR | 2.373 % | 129.1407 | 55.09 % | 68.75 % | 75.28 % | 80.89 % | 85.67 % | 89.53 % |
| 0.5 ATR | 3.39 % | 127.7954 | 38.27 % | 55.24 % | 63.37 % | 71.28 % | 78.46 % | 84.7 % |
| 0.75 ATR | 5.085 % | 125.553 | 19.44 % | 37.7 % | 47.12 % | 58.04 % | 67.99 % | 77.21 % |
| 1.0 ATR | 6.781 % | 123.3107 | 9.37 % | 25.3 % | 34.91 % | 46.61 % | 58.94 % | 70.43 % |
| 1.25 ATR | 8.476 % | 121.0684 | 4.13 % | 14.62 % | 25.13 % | 36.1 % | 49.9 % | 62.94 % |
| 1.5 ATR | 10.171 % | 118.8261 | 2.11 % | 8.77 % | 17.46 % | 29.12 % | 43.09 % | 57.08 % |
| 2.0 ATR | 13.561 % | 114.3414 | 0.2 % | 3.12 % | 7.37 % | 16.18 % | 31.3 % | 47.23 % |
| 2.5 ATR | 16.951 % | 109.8568 | 0.1 % | 0.91 % | 2.42 % | 8.7 % | 21.44 % | 37.58 % |
| 3.0 ATR | 20.342 % | 105.3721 | 0.1 % | 0.5 % | 1.01 % | 4.55 % | 14.53 % | 28.03 % |
| 4.0 ATR | 27.122 % | 96.4029 | 0.0 % | 0.0 % | 0.3 % | 0.81 % | 6.2 % | 18.07 % |
| 6.0 ATR | 40.683 % | 78.4643 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.61 % | 4.41 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.19 ATR | 0.40 ATR | 0.44 ATR | 0.57 ATR | 0.68 ATR | 0.74 ATR | 0.98 ATR | 1.21 ATR |
| **2 s.** | 0.28 ATR | 0.57 ATR | 0.65 ATR | 0.84 ATR | 1.01 ATR | 1.12 ATR | 1.45 ATR | 1.83 ATR |
| **3 s.** | 0.35 ATR | 0.71 ATR | 0.79 ATR | 1.05 ATR | 1.25 ATR | 1.42 ATR | 1.87 ATR | 2.24 ATR |
| **5 s.** | 0.44 ATR | 0.93 ATR | 1.04 ATR | 1.36 ATR | 1.66 ATR | 1.85 ATR | 2.41 ATR | 2.95 ATR |
| **10 s.** | 0.58 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.32 ATR | 2.60 ATR | 3.54 ATR | 4.43 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.74 ATR | 3.30 ATR | 3.81 ATR | 5.18 ATR | 5.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.44–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.39 %, prix 127.7957), p(touche) 38.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.646–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.085 %, prix 125.5536), p(touche) 37.7 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.793–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.781 %, prix 123.3101), p(touche) 34.91 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.038–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.476 %, prix 121.0679), p(touche) 36.1 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.43–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.171 %, prix 118.8258), p(touche) 43.09 % (en stress 100.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.116–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (16.951 %, prix 109.8572), p(touche) 37.58 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 44.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : $0.082 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 18 % | T3 18 %
- Kelly (position) : f* 0.084 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.0 | bear 64.5 | side 23.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 265.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.808% → cible +3.415% / stop −3.5%, p_fill 35%, n_eff≈15.9) : P(cible|rempli) **26%** · **EV/risk +0.055** (×p_fill ; si rempli +0.55% du capital)
  - **swing** (entrée dip −6.19% → cible +9.794% / stop −7.228%, p_fill 11%, n_eff≈15.8) : P(cible|rempli) **24%** · **EV/risk -0.010** (×p_fill ; si rempli -0.63% du capital)
  - **deep** (entrée dip −9.559% → cible +27.313% / stop −13.656%, p_fill 12%, n_eff≈14.3) : P(cible|rempli) **0%** · **EV/risk -0.034** (×p_fill ; si rempli -3.76% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 47.1  _(neutre)_
- **ADX** : 37.5  _(tendance etablie)_
- **MACD** : hist -1.166  _(bearish_recent)_
- **BB** : %B 0.59 · largeur 24.3%
- **ATR** : 8.97 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.172  _(accumulation)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 63.4  _(marche en range (choppy))_
- **MA** : MA20 129.57 · MA50 109.62 · MA200 137.13  _(prix > MA20)_
- **Dist MA** : MA20 +2.1% · MA50 +20.7% · MA200 -3.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (771607 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
