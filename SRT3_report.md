# SRT3

**Generated** : 2026-08-25T00:03:34.315099+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €244.50  

> 🟡 **WAIT-FOR-DIP** — spot +4.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €244.50 (+4.8% vs entrée) · entrée €233.37 · stop €225.84 · T1 €239.44 · R/R 0.81  
> ↳ P(T1 av. stop) 64 % · EV/risk 0.08 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €232.16–€234.59 (mid €233.37)
- Spot actuel : €244.50 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : €225.84 (stop swing_plan-based (-7.63%))
- Targets : T1 €239.44 · R/R 0.81 | T2 €245.51 · R/R 1.61 | T3 €251.57 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €225.84


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.18 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.63 %)** : le gap seul le franchit 0.392 % des séances (5 fois sur 1274).
   - exécution **2.027 pt plus bas** dans le cas TYPIQUE (médiane), 4.882 au p90, **6.575 au pire**
   - perte réelle **10.096 %** en moyenne _(tirée par la queue)_, jusqu'à **14.205 %** — au lieu des 7.63 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0097 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.616 % | p01 -3.24 % | pire -14.205 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0368** [0.0159 ; 0.0729] _(largeur 5.7 pt, n_eff 173.1)_
   - swing : **0.3494** [0.3006 ; 0.4007] _(largeur 10.0 pt, n_eff 345.8)_
   - deep : **0.4816** [0.4293 ; 0.5342] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1260 séances)** : VaR **-4.12 %** | CVaR **-6.6 %** | vol 2.85 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.0 % vs -9.25 % si l'on extrapolait par √5 _(rapport 1.081 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0659** (β de hausse 1.1723, asymétrie 0.9093) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.359× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 222.1322 sur grid_snapped (2.67 ATR, 9.148 %) — p(stop avant cible) 0.1819 [0.14 ; 0.23], R/R 0.257, perte reelle 11.278 % (gap inclus), CVaR 9.153 %, EV -0.377 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.26 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 4.623 %) — p(stop avant cible) 0.3973 [0.35 ; 0.45], R/R 0.364, perte reelle 7.948 % (gap inclus), EV -1.4525 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.45 %) : P(cible) 59.2 % x 2.89 % + P(rien) 1.1 % x -0.70 % ne couvrent pas P(stop) 39.7 % x 7.95 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 2.67 ATR (stop 10.107 %) — p(stop avant cible) 0.1571 [0.12 ; 0.20], R/R 0.204, perte reelle 14.205 % (gap inclus), EV -0.6308 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 71.6 % x 2.89 % + P(rien) 12.7 % x -3.69 % ne couvrent pas P(stop) 15.7 % x 14.20 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 7.68 ATR (stop 25.541 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.113, perte reelle 25.541 % (gap inclus), EV 0.249 % — **REFUSE**
      - refuse : R/R 0.11 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.54 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 3.082 %) — p(stop avant cible) 0.471 [0.42 ; 0.52], R/R 0.411, perte reelle 7.038 % (gap inclus), EV -1.7942 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.79 %) : P(cible) 52.6 % x 2.89 % + P(rien) 0.3 % x -0.67 % ne couvrent pas P(stop) 47.1 % x 7.04 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 3.853 %) — p(stop avant cible) 0.4211 [0.37 ; 0.47], R/R 0.377, perte reelle 7.669 % (gap inclus), EV -1.5792 % — **REFUSE**
      - refuse : R/R 0.38 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.58 %) : P(cible) 57.2 % x 2.89 % + P(rien) 0.7 % x -0.47 % ne couvrent pas P(stop) 42.1 % x 7.67 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 6.164 %) — p(stop avant cible) 0.2989 [0.25 ; 0.35], R/R 0.312, perte reelle 9.276 % (gap inclus), EV -0.8952 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 66.5 % x 2.89 % + P(rien) 3.6 % x -1.31 % ne couvrent pas P(stop) 29.9 % x 9.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ grid_snapped a 2.67 ATR (stop 9.148 %) — p(stop avant cible) 0.1819 [0.14 ; 0.23], R/R 0.257, perte reelle 11.278 % (gap inclus), EV -0.377 % — **REFUSE**
      - refuse : R/R 0.26 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 71.3 % x 2.89 % + P(rien) 10.5 % x -3.71 % ne couvrent pas P(stop) 18.2 % x 11.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 12.328 %) — p(stop avant cible) 0.0922 [0.07 ; 0.13], R/R 0.204, perte reelle 14.205 % (gap inclus), EV -0.0918 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.33 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 72.1 % x 2.89 % + P(rien) 18.7 % x -4.63 % ne couvrent pas P(stop) 9.2 % x 14.21 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 13.869 %) — p(stop avant cible) 0.0644 [0.04 ; 0.09], R/R 0.204, perte reelle 14.205 % (gap inclus), EV 0.0763 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.87 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 15.41 %) — p(stop avant cible) 0.0408 [0.02 ; 0.07], R/R 0.188, perte reelle 15.41 % (gap inclus), EV 0.1023 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.41 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 16.952 %) — p(stop avant cible) 0.0122 [0.00 ; 0.03], R/R 0.171, perte reelle 16.952 % (gap inclus), EV 0.2217 % — **REFUSE**
      - refuse : R/R 0.17 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.95 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 18.493 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 0.156, perte reelle 18.493 % (gap inclus), EV 0.2044 % — **REFUSE**
      - refuse : R/R 0.16 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.49 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 20.034 %) — p(stop avant cible) 0.0092 [0.00 ; 0.02], R/R 0.144, perte reelle 20.034 % (gap inclus), EV 0.2057 % — **REFUSE**
      - refuse : R/R 0.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.03 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 21.575 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.134, perte reelle 21.575 % (gap inclus), EV 0.2322 % — **REFUSE**
      - refuse : R/R 0.13 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.57 % > budget 12.00 %
   - 🟢 grid_snapped a 7.68 ATR (stop 24.582 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.118, perte reelle 24.582 % (gap inclus), EV 0.2492 % — **REFUSE**
      - refuse : R/R 0.12 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.58 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.022 | EV/share : €-0.168 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 30 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 15.5 | bear 7.7 | side 76.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 489.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.072% → cible +3.379% / stop −3.0%, p_fill 34%, n_eff≈14.7) : P(cible|rempli) **21%** · **EV/risk +0.119** (×p_fill ; si rempli +1.04% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→78% · +2.0%→48% · +3.0%→25% · +5.0%→4% · +8.0%→0%
- Range intraday médian 3.33% (p90 6.3%) · excursion haute méd. +1.89% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.035% vs midi 0.845% vs clôture 0.994% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; neutre — autocorr -0.021)_ ; drift intra méd. 0.147% ; recovery-V 26%
- **σ réalisé intraday** 2.532% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 70% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 244.5125 (VA 243.7725–245.6225 ; dernier close 246.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 72% · **stop −2.11%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.06% · baisse 49% (gap-down >1% 13% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.44% (p90 −1.81%) · haut méd +0.53% · range méd 1.21%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −1.91%) · haut méd +0.64% · range méd 1.49%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.04%) · haut méd +0.8% · range méd 1.71%
- Excursion ouverture 60min (n=160) : bas méd −0.75% (p90 −2.45%) · haut méd +0.82% · range méd 1.83%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 246.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 76% (125/159) · gap 25% · délai 0.2min · rebond 53% (64/125) (MFE +1.16%)
   - −1.0% : fill 30min 44% · séance 65% (106/159) · gap 13% · délai 1.6min · rebond 58% (59/106) (MFE +1.16%)
   - −1.5% : fill 30min 34% · séance 58% (97/159) · gap 6% · délai 5.0min · rebond 72% (62/97) (MFE +1.57%)
   - −2.0% : fill 30min 18% · séance 40% (75/159) · gap 3% · délai 94.7min · rebond 60% (45/75) (MFE +1.61%)
   - −3.0% : fill 30min 6% · séance 18% (40/159) · gap 1% · délai 184.6min · rebond 62% (24/40) (MFE +1.94%)
   - −4.0% : fill 30min 3% · séance 9% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 6% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.44% (p90 −1.97%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −2.24%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.59%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=446 jambes) : jambe baissière méd −1.04% (p90 −2.34%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 82% (58/69) · rebond 68% (36/58)
      · −2.0% : fill 53% (43/69) · rebond 53% (26/43)
      · −3.0% : fill 30% (28/69) · rebond 57% (16/28)
      · −4.0% : fill 12% (15/69) · rebond 71% (11/15)
      · −5.0% : fill 6% (7/69) · rebond 92% (6/7)
   - **flat** (33 séances) :
      · −1.0% : fill 68% (21/33) · rebond 54% (10/21)
      · −2.0% : fill 47% (16/33) · rebond 62% (8/16)
      · −3.0% : fill 16% (6/33) · rebond 66% (4/6)
      · −4.0% : fill 12% (4/33) · rebond 70% (3/4)
      · −5.0% : fill 12% (4/33) · rebond 24% (2/4)
   - **gap-up** (57 séances) :
      · −1.0% : fill 47% (27/57) · rebond 45% (13/27)
      · −2.0% : fill 22% (16/57) · rebond 77% (11/16)
      · −3.0% : fill 6% (6/57) · rebond 78% (4/6)
      · −4.0% : fill 4% (2/57) · rebond 100% (2/2)
      · −5.0% : fill 3% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 57% si les 15 1res min sont vertes (87 cas) · 37% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 57% si début vert vs 38% si rouge (base 48% · écart 19 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **57%** · continue >prix actuel 46% ; creux résiduel méd -1.43% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.36% → **scale +1.34% / runner +2.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **38%** (continue à baisser 52%) → **RÉDUIRE ~62%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.51%** (au-delà de la MAE q10 -4.51%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +2.12%] · haut q95 +2.63% · bas q05 -3.25%
   - 60min (n=160) : retour [-2.58% .. +2.34%] · haut q95 +2.83% · bas q05 -3.66%
   - 2h (n=160) : retour [-2.18% .. +2.49%] · haut q95 +2.94% · bas q05 -3.82%
   - 4h (n=160) : retour [-2.52% .. +2.28%] · haut q95 +3.26% · bas q05 -3.83%
   - 6h (n=160) : retour [-2.57% .. +2.94%] · haut q95 +3.61% · bas q05 -3.92%
   - session (n=160) : retour [-3.59% .. +4.13%] · haut q95 +5.59% · bas q05 -4.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 66.9  _(momentum haussier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 1.613  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 14.3%
- **ATR** : 7.54 (26.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.028  _(neutre)_
- **Vol ratio** : 0.2  _(volume atone)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 232.74 · MA50 230.24 · MA200 232.04  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 +6.2% · MA200 +5.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (804784 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
