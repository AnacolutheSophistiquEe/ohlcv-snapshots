# SMCI

**Generated** : 2026-09-04T00:26:41.526634+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · $37.87  

> 🟡 **WAIT-FOR-DIP** — spot +4.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $37.87 (+4.2% vs entrée) · entrée $36.34 · stop $35.62 · T1 $37.37 · R/R 1.43  
> ↳ P(T1 av. stop) 46 % _(réel 5 s)_ · EV/risk 0.032 _(réel 5 s)_ (GBM 0.056) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché -5.4 % ≠ (strike 35.0 − spot 37.87)/spot = -7.6 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 240 % hors [0,100] (R² max 0.88). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $36.14–$36.55 (mid $36.34)
- Spot actuel : $37.87 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $35.62 (stop swing_plan-based (-15.94%))
- Targets : T1 $37.37 · R/R 1.43 | T2 $38.40 · R/R 2.86 | T3 $39.43 · R/R 4.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $35.62


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.74 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.94 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **8.717 pt plus bas** dans le cas TYPIQUE (médiane), 12.235 au p90, **13.111 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 15.94 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0298 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.765 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5375** [0.4631 ; 0.6106] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4123** [0.3613 ; 0.4647] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.3849** [0.3347 ; 0.437] _(largeur 10.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (48.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.54 %** | CVaR **-12.28 %** | vol 5.76 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 4.24 % contre 7.19 % aujourd'hui, rapport 0.59)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -16.69 % vs -16.05 % si l'on extrapolait par √5 _(rapport 1.04 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5394** (β de hausse 1.2423, asymétrie 1.2391) vs IWM — 602 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.968× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 34.6193 sur atr_based (1.5 ATR, 8.584 %) — p(stop avant cible) 0.4949 [0.44 ; 0.55], R/R 1.703, perte reelle 14.137 % (gap inclus), CVaR 8.673 %, EV -0.7211 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 15 des 15 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 65.4 % de la queue et il ne reste que -955.87 EUR a partager. Prix du risque -0.692 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 8.584 %) — p(stop avant cible) 0.4949 [0.44 ; 0.55], R/R 1.703, perte reelle 14.137 % (gap inclus), EV -0.7211 % — **REFUSE**
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.72 %) : P(cible) 20.9 % x 24.07 % + P(rien) 29.6 % x 4.22 % ne couvrent pas P(stop) 49.5 % x 14.14 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 1.94 ATR (stop 13.93 %) — p(stop avant cible) 0.2671 [0.22 ; 0.32], R/R 1.156, perte reelle 20.821 % (gap inclus), EV 0.4264 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.97 % > budget 12.00 %
   - ⚪ sr_based a 2.92 ATR (stop 19.487 %) — p(stop avant cible) 0.1537 [0.12 ; 0.19], R/R 0.896, perte reelle 26.856 % (gap inclus), EV 1.3445 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.50 % > budget 12.00 %
   - 🟢 support a 4.69 ATR (stop 29.633 %) — p(stop avant cible) 0.0871 [0.06 ; 0.12], R/R 0.812, perte reelle 29.633 % (gap inclus), EV 1.806 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.63 % > budget 12.00 %
   - 🟢 support a 5.75 ATR (stop 35.706 %) — p(stop avant cible) 0.0674 [0.04 ; 0.10], R/R 0.674, perte reelle 35.706 % (gap inclus), EV 1.4769 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.71 % > budget 12.00 %
   - 🟢 support a 6.69 ATR (stop 41.067 %) — p(stop avant cible) 0.0135 [0.01 ; 0.03], R/R 0.586, perte reelle 41.067 % (gap inclus), EV 1.7233 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.07 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.431 %) — p(stop avant cible) 0.9076 [0.87 ; 0.93], R/R 6.292, perte reelle 3.826 % (gap inclus), EV -1.5612 % — **REFUSE**
      - refuse : cible atteinte seulement 7.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.908, borne haute 0.935 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.56 %) : P(cible) 7.0 % x 24.07 % + P(rien) 2.3 % x 10.40 % ne couvrent pas P(stop) 90.8 % x 3.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.5 ATR (stop 2.861 %) — p(stop avant cible) 0.8178 [0.77 ; 0.86], R/R 3.99, perte reelle 6.034 % (gap inclus), EV -1.5336 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.818, borne haute 0.856 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.53 %) : P(cible) 12.0 % x 24.07 % + P(rien) 6.2 % x 8.29 % ne couvrent pas P(stop) 81.8 % x 6.03 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 0.75 ATR (stop 4.292 %) — p(stop avant cible) 0.7234 [0.67 ; 0.77], R/R 2.74, perte reelle 8.786 % (gap inclus), EV -1.7652 % — **REFUSE**
      - refuse : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.77 %) : P(cible) 15.5 % x 24.07 % + P(rien) 12.1 % x 7.02 % ne couvrent pas P(stop) 72.3 % x 8.79 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 5.723 %) — p(stop avant cible) 0.6518 [0.60 ; 0.70], R/R 2.075, perte reelle 11.6 % (gap inclus), EV -2.1402 % — **REFUSE**
      - refuse : p_stop_first 0.652, borne haute 0.701 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.08 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.14 %) : P(cible) 18.3 % x 24.07 % + P(rien) 16.5 % x 6.12 % ne couvrent pas P(stop) 65.2 % x 11.60 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 7.153 %) — p(stop avant cible) 0.5839 [0.53 ; 0.64], R/R 1.777, perte reelle 13.549 % (gap inclus), EV -2.0918 % — **REFUSE**
      - refuse : p_stop_first 0.584, borne haute 0.635 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.09 %) : P(cible) 19.2 % x 24.07 % + P(rien) 22.4 % x 5.33 % ne couvrent pas P(stop) 58.4 % x 13.55 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 1.94 ATR (stop 12.843 %) — p(stop avant cible) 0.3115 [0.26 ; 0.36], R/R 1.252, perte reelle 19.221 % (gap inclus), EV 0.1706 % — **REFUSE**
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.89 % > budget 12.00 %
   - ⚪ grid_snapped a 2.92 ATR (stop 18.399 %) — p(stop avant cible) 0.1655 [0.13 ; 0.21], R/R 0.966, perte reelle 24.92 % (gap inclus), EV 1.408 % — **REFUSE**
      - refuse : R/R 0.97 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.42 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 22.89 %) — p(stop avant cible) 0.1264 [0.09 ; 0.16], R/R 0.896, perte reelle 26.856 % (gap inclus), EV 1.7359 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.90 % > budget 12.00 %
   - 🟢 grid_snapped a 4.69 ATR (stop 28.545 %) — p(stop avant cible) 0.0893 [0.06 ; 0.12], R/R 0.829, perte reelle 29.051 % (gap inclus), EV 1.8526 % — **REFUSE**
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.55 % > budget 12.00 %
   - 🟢 grid_snapped a 5.75 ATR (stop 34.619 %) — p(stop avant cible) 0.0708 [0.05 ; 0.10], R/R 0.695, perte reelle 34.619 % (gap inclus), EV 1.5203 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.62 % > budget 12.00 %
   - 🟢 grid_snapped a 6.69 ATR (stop 39.979 %) — p(stop avant cible) 0.0165 [0.01 ; 0.03], R/R 0.602, perte reelle 39.979 % (gap inclus), EV 1.7134 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.98 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 42.919 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.561, perte reelle 42.919 % (gap inclus), EV 1.7411 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 42.92 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 45.781 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.526, perte reelle 45.781 % (gap inclus), EV 1.7379 % — **REFUSE**
      - refuse : R/R 0.53 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.78 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 37.87, ATR14 2.1671 (5.723 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.346 ATR = 1.98 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.286 % | 37.7616 | 90.43 % | 93.15 % | 94.55 % | 95.05 % | 96.34 % | 97.54 % |
| 0.1 ATR | 0.572 % | 37.6533 | 82.18 % | 87.1 % | 89.1 % | 91.1 % | 92.99 % | 94.87 % |
| 0.15 ATR | 0.858 % | 37.5449 | 75.03 % | 81.96 % | 84.86 % | 88.07 % | 90.55 % | 93.63 % |
| 0.2 ATR | 1.145 % | 37.4366 | 68.08 % | 77.22 % | 80.42 % | 85.54 % | 89.13 % | 92.3 % |
| 0.25 ATR | 1.431 % | 37.3282 | 62.03 % | 72.68 % | 76.29 % | 82.2 % | 87.09 % | 90.55 % |
| 0.35 ATR | 2.003 % | 37.1115 | 49.45 % | 63.51 % | 69.73 % | 77.25 % | 82.72 % | 87.99 % |
| 0.5 ATR | 2.861 % | 36.7864 | 34.94 % | 50.0 % | 58.32 % | 68.76 % | 76.93 % | 83.88 % |
| 0.75 ATR | 4.292 % | 36.2446 | 17.32 % | 33.27 % | 42.99 % | 55.11 % | 66.46 % | 75.77 % |
| 1.0 ATR | 5.723 % | 35.7029 | 8.06 % | 21.77 % | 30.78 % | 43.88 % | 57.42 % | 68.79 % |
| 1.25 ATR | 7.153 % | 35.1611 | 3.83 % | 15.02 % | 22.7 % | 33.47 % | 48.48 % | 61.81 % |
| 1.5 ATR | 8.584 % | 34.6193 | 1.51 % | 9.68 % | 16.45 % | 26.39 % | 42.17 % | 55.34 % |
| 2.0 ATR | 11.445 % | 33.5357 | 0.3 % | 3.53 % | 8.38 % | 16.08 % | 30.08 % | 44.05 % |
| 2.5 ATR | 14.306 % | 32.4521 | 0.2 % | 1.51 % | 4.34 % | 9.81 % | 19.82 % | 32.03 % |
| 3.0 ATR | 17.168 % | 31.3686 | 0.2 % | 1.21 % | 2.62 % | 5.66 % | 14.23 % | 24.13 % |
| 4.0 ATR | 22.89 % | 29.2014 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 34.336 % | 24.8671 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.95 ATR | 1.18 ATR |
| **2 s.** | 0.22 ATR | 0.50 ATR | 0.57 ATR | 0.76 ATR | 0.93 ATR | 1.07 ATR | 1.49 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.18 ATR | 1.36 ATR | 1.90 ATR | 2.42 ATR |
| **5 s.** | 0.39 ATR | 0.86 ATR | 0.97 ATR | 1.27 ATR | 1.57 ATR | 1.81 ATR | 2.48 ATR | 3.22 ATR |
| **10 s.** | 0.55 ATR | 1.21 ATR | 1.39 ATR | 1.88 ATR | 2.25 ATR | 2.49 ATR | 3.62 ATR | 4.90 ATR |
| **20 s.** | 0.78 ATR | 1.74 ATR | 1.96 ATR | 2.46 ATR | 2.94 ATR | 3.42 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.396–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.575–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.292 %, prix 36.2446), p(touche) 33.27 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.717–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.292 %, prix 36.2446), p(touche) 42.99 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.975–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (7.153 %, prix 35.1612), p(touche) 33.47 % (en stress 89.9 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.388–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (8.584 %, prix 34.6192), p(touche) 42.17 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.958–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 3.0 ATR (17.168 %, prix 31.3685), p(touche) 24.13 % (en stress 96.94 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.4 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.056 | EV/share : $0.041 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.047 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 84.4 | bear 5.2 | side 10.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 379.0 (= 10 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.031% → cible +2.83% / stop −2.0%, p_fill 23%, n_eff≈13.9) : P(cible|rempli) **46%** · **EV/risk +0.032** (×p_fill ; si rempli +0.27% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=9))
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→76% · +2.0%→60% · +3.0%→45% · +5.0%→28% · +8.0%→12%
- Range intraday médian 6.14% (p90 10.79%) · excursion haute méd. +2.53% / basse méd. −2.38%
- Profil de vol intra : ouverture 4.146% vs midi 1.257% vs clôture 1.632% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓1% ; spike-down 71% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. 0.072% ; recovery-V 34%
- **σ réalisé intraday** 3.89% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 68% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 36.4477 (VA 36.1638–36.8028 ; dernier close 36.71)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 81% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.59% · R/R 0.62 (high win-rate)
- Gaps overnight (n=159) : méd. 0.16% · baisse 46% (gap-down >1% 36% · >2% 18%)
- Excursion ouverture 5min (n=160) : bas méd −0.88% (p90 −2.79%) · haut méd +1.02% · range méd 2.23%
- Excursion ouverture 15min (n=160) : bas méd −1.26% (p90 −3.28%) · haut méd +1.46% · range méd 2.94%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.82%) · haut méd +1.56% · range méd 3.7%
- Excursion ouverture 60min (n=160) : bas méd −1.68% (p90 −4.43%) · haut méd +1.84% · range méd 4.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 36.71 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 73% (120/159) · gap 42% · délai 0.0min · rebond 56% (72/120) (MFE +1.26%)
   - −1.0% : fill 30min 55% · séance 69% (111/159) · gap 36% · délai 0.0min · rebond 60% (65/111) (MFE +1.38%)
   - −1.5% : fill 30min 48% · séance 63% (101/159) · gap 24% · délai 0.0min · rebond 69% (64/101) (MFE +1.56%)
   - −2.0% : fill 30min 44% · séance 55% (88/159) · gap 18% · délai 0.2min · rebond 72% (58/88) (MFE +1.73%)
   - −3.0% : fill 30min 31% · séance 49% (76/159) · gap 10% · délai 8.8min · rebond 61% (47/76) (MFE +1.78%)
   - −4.0% : fill 30min 18% · séance 38% (57/159) · gap 6% · délai 36.7min · rebond 78% (38/57) (MFE +1.88%)
   - −5.0% : fill 30min 13% · séance 29% (46/159) · gap 4% · délai 42.5min · rebond 81% (34/46) (MFE +2.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.81%) → stop au-delà de −1.89% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −2.98%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.83%) → stop au-delà de −1.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=899 jambes) : jambe baissière méd −1.2% (p90 −2.86%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 97% (68/70) · rebond 48% (35/68)
      · −2.0% : fill 92% (64/70) · rebond 69% (39/64)
      · −3.0% : fill 85% (58/70) · rebond 57% (34/58)
      · −4.0% : fill 68% (45/70) · rebond 78% (30/45)
      · −5.0% : fill 51% (37/70) · rebond 80% (27/37)
   - **flat** (13 séances) :
      · −1.0% : fill 100% (13/13) · rebond 92% (11/13)
      · −2.0% : fill 41% (6/13) · rebond 89% (4/6)
      · −3.0% : fill 26% (3/13) · rebond 100% (3/3)
      · −4.0% : fill 22% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (76 séances) :
      · −1.0% : fill 40% (30/76) · rebond 74% (19/30)
      · −2.0% : fill 22% (18/76) · rebond 81% (15/18)
      · −3.0% : fill 18% (15/76) · rebond 70% (10/15)
      · −4.0% : fill 13% (10/76) · rebond 71% (6/10)
      · −5.0% : fill 12% (9/76) · rebond 85% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 65% si les 15 1res min sont vertes (77 cas) · 26% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 45% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **72%** · continue >prix actuel 45% ; creux résiduel méd -2.21% (q20 -3.74%) → **SL/trailing à −3.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.03% / q75 +3.98% → **scale +2.03% / runner +3.98%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **20%** (continue à baisser 50%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.24% .. +4.68%] · haut q95 +5.97% · bas q05 -4.53%
   - 60min (n=160) : retour [-4.5% .. +5.32%] · haut q95 +6.54% · bas q05 -5.34%
   - 2h (n=160) : retour [-4.71% .. +6.65%] · haut q95 +7.61% · bas q05 -5.85%
   - 4h (n=160) : retour [-5.21% .. +7.13%] · haut q95 +8.57% · bas q05 -6.74%
   - 6h (n=160) : retour [-5.68% .. +6.82%] · haut q95 +9.28% · bas q05 -6.91%
   - session (n=160) : retour [-6.84% .. +7.77%] · haut q95 +9.38% · bas q05 -7.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.61%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.4  _(momentum baissier)_
- **ADX** : 24.3  _(pas de tendance nette)_
- **MACD** : hist -0.193  _(bearish_recent)_
- **BB** : %B 0.63 · largeur 26.9%
- **ATR** : 2.17 (44.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.051  _(accumulation)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 65.3  _(marche en range (choppy))_
- **MA** : MA20 36.61 · MA50 31.55 · MA200 31.34  _(prix > MA20)_
- **Dist MA** : MA20 +3.4% · MA50 +20.0% · MA200 +20.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (750974 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
