# SAF

**Generated** : 2026-08-24T00:07:37.730688+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €343.60  

> 🟡 **WAIT-FOR-DIP** — spot +8.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €343.60 (+8.8% vs entrée) · entrée €315.82 · stop €308.87 · T1 €321.60 · R/R 0.83  
> ↳ P(T1 av. stop) 54 % · EV/risk 0.031 · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €314.66–€316.97 (mid €315.82)
- Spot actuel : €343.60 (+8.8% au-dessus de la zone — repli à attendre)
- Stop : €308.87 (stop swing_plan-based (-10.11%))
- Targets : T1 €321.60 · R/R 0.83 | T2 €327.38 · R/R 1.66 | T3 €333.17 · R/R 2.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €308.87


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (10.11 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 10.11 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0121** [0.0026 ; 0.0374] _(largeur 3.5 pt, n_eff 173.1)_
   - swing : **0.1493** [0.1147 ; 0.1897] _(largeur 7.5 pt, n_eff 345.8)_
   - deep : **0.2514** [0.2079 ; 0.2991] _(largeur 9.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.05 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.33 % contre 2.50 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.63 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.928 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3705** (β de hausse 1.3391, asymétrie 1.0235) vs FCHI — 617 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.263× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 308.85 sur atr_grid (5.0 ATR, 10.114 %) — p(stop avant cible) 0.0836 [0.06 ; 0.12], R/R 0.517, perte reelle 10.114 % (gap inclus), CVaR 10.114 %, EV 0.8656 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 3.034 %) — p(stop avant cible) 0.4342 [0.38 ; 0.49], R/R 1.087, perte reelle 4.809 % (gap inclus), EV 0.0331 % — **REFUSE**
      - refuse : R/R 1.09 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 7.37 ATR (stop 16.221 %) — p(stop avant cible) 0.0071 [0.00 ; 0.02], R/R 0.322, perte reelle 16.221 % (gap inclus), EV 0.8392 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.22 % > budget 12.00 %
   - 🟢 support a 12.07 ATR (stop 25.74 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.203, perte reelle 25.74 % (gap inclus), EV 0.8542 % — **REFUSE**
      - refuse : R/R 0.20 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.74 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 2.023 %) — p(stop avant cible) 0.5827 [0.53 ; 0.63], R/R 1.675, perte reelle 3.121 % (gap inclus), EV -0.0803 % — **REFUSE**
      - refuse : p_stop_first 0.583, borne haute 0.634 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 29.3 % x 5.23 % + P(rien) 12.4 % x 1.65 % ne couvrent pas P(stop) 58.3 % x 3.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.25 ATR (stop 2.528 %) — p(stop avant cible) 0.5102 [0.46 ; 0.56], R/R 1.27, perte reelle 4.117 % (gap inclus), EV -0.1969 % — **REFUSE**
      - refuse : p_stop_first 0.510, borne haute 0.563 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.27 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.20 %) : P(cible) 32.0 % x 5.23 % + P(rien) 17.0 % x 1.36 % ne couvrent pas P(stop) 51.0 % x 4.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 4.045 %) — p(stop avant cible) 0.3178 [0.27 ; 0.37], R/R 0.848, perte reelle 6.163 % (gap inclus), EV 0.3238 % — **REFUSE**
      - refuse : R/R 0.85 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.551 %) — p(stop avant cible) 0.2832 [0.24 ; 0.33], R/R 0.769, perte reelle 6.799 % (gap inclus), EV 0.3709 % — **REFUSE**
      - refuse : R/R 0.77 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 5.057 %) — p(stop avant cible) 0.2476 [0.20 ; 0.30], R/R 0.68, perte reelle 7.683 % (gap inclus), EV 0.4264 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 6.068 %) — p(stop avant cible) 0.2079 [0.17 ; 0.25], R/R 0.524, perte reelle 9.986 % (gap inclus), EV 0.2949 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 7.079 %) — p(stop avant cible) 0.153 [0.12 ; 0.19], R/R 0.524, perte reelle 9.986 % (gap inclus), EV 0.578 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 8.091 %) — p(stop avant cible) 0.1266 [0.09 ; 0.16], R/R 0.524, perte reelle 9.986 % (gap inclus), EV 0.7448 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 9.102 %) — p(stop avant cible) 0.1006 [0.07 ; 0.14], R/R 0.524, perte reelle 9.986 % (gap inclus), EV 0.8387 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 10.114 %) — p(stop avant cible) 0.0836 [0.06 ; 0.12], R/R 0.517, perte reelle 10.114 % (gap inclus), EV 0.8656 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 11.125 %) — p(stop avant cible) 0.0648 [0.04 ; 0.09], R/R 0.47, perte reelle 11.125 % (gap inclus), EV 0.8567 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.0 ATR (stop 12.136 %) — p(stop avant cible) 0.0494 [0.03 ; 0.08], R/R 0.431, perte reelle 12.136 % (gap inclus), EV 0.8578 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.14 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 13.148 %) — p(stop avant cible) 0.0355 [0.02 ; 0.06], R/R 0.398, perte reelle 13.148 % (gap inclus), EV 0.8325 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.15 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 14.159 %) — p(stop avant cible) 0.0239 [0.01 ; 0.04], R/R 0.369, perte reelle 14.159 % (gap inclus), EV 0.8199 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.16 % > budget 12.00 %
   - ⚪ grid_snapped a 7.37 ATR (stop 15.511 %) — p(stop avant cible) 0.0103 [0.00 ; 0.03], R/R 0.337, perte reelle 15.511 % (gap inclus), EV 0.8301 % — **REFUSE**
      - refuse : R/R 0.34 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.51 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : €0.214 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 32 % | T3 18 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.1 | bear 9.9 | side 85.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 344.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→52% · +2.0%→28% · +3.0%→10% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.52% (p90 3.76%) · excursion haute méd. +1.09% / basse méd. −0.91%
- Profil de vol intra : ouverture 1.55% vs midi 0.565% vs clôture 0.698% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 43% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -0.197% ; recovery-V 17%
- **σ réalisé intraday** 1.597% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 55% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 341.4488 (VA 341.1938–342.9787 ; dernier close 343.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 30% · rebond 46% · **stop −1.99%** sous le fill (sous le bruit) · cible +0.81% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.14% · baisse 45% (gap-down >1% 7% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.42% (p90 −1.51%) · haut méd +0.17% · range méd 0.91%
- Excursion ouverture 15min (n=160) : bas méd −0.5% (p90 −1.83%) · haut méd +0.25% · range méd 1.09%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −1.89%) · haut méd +0.5% · range méd 1.28%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −1.92%) · haut méd +0.56% · range méd 1.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 343.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 68% (113/159) · gap 17% · délai 0.3min · rebond 37% (43/113) (MFE +0.73%)
   - −1.0% : fill 30min 37% · séance 52% (87/159) · gap 7% · délai 1.5min · rebond 41% (33/87) (MFE +0.61%)
   - −1.5% : fill 30min 22% · séance 39% (71/159) · gap 3% · délai 18.9min · rebond 39% (26/71) (MFE +0.81%)
   - −2.0% : fill 30min 10% · séance 30% (53/159) · gap 1% · délai 56.2min · rebond 46% (24/53) (MFE +0.81%)
   - −3.0% : fill 30min 2% · séance 14% (29/159) · gap 0% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 1% · séance 6% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −0.78%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.12% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=211 jambes) : jambe baissière méd −1.03% (p90 −2.28%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 80% (45/55) · rebond 38% (17/45)
      · −2.0% : fill 59% (32/55) · rebond 44% (15/32)
      · −3.0% : fill 26% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 13% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (42 séances) :
      · −1.0% : fill 48% (21/42) · rebond 55% (11/21)
      · −2.0% : fill 23% (10/42) · rebond 55% (5/10)
      · −3.0% : fill 8% (5/42) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/42) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/42) · rebond 0% (0/0)
   - **gap-up** (62 séances) :
      · −1.0% : fill 32% (21/62) · rebond 31% (5/21)
      · −2.0% : fill 12% (11/62) · rebond 43% (4/11)
      · −3.0% : fill 8% (7/62) · rebond 36% (4/7)
      · −4.0% : fill 3% (3/62) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/62) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 65% si les 15 1res min sont vertes (75 cas) · 29% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 47% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 288min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -0.74% (q20 -1.51%) → **SL/trailing à −1.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.75% / q75 +1.53% → **scale +0.75% / runner +1.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 50%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.33%** (au-delà de la MAE q10 -2.33%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.56% .. +1.57%] · haut q95 +1.97% · bas q05 -2.17%
   - 60min (n=160) : retour [-1.64% .. +2.12%] · haut q95 +2.19% · bas q05 -2.47%
   - 2h (n=160) : retour [-2.07% .. +2.15%] · haut q95 +2.56% · bas q05 -2.94%
   - 4h (n=160) : retour [-1.88% .. +2.19%] · haut q95 +2.77% · bas q05 -3.01%
   - 6h (n=160) : retour [-2.15% .. +2.38%] · haut q95 +3.11% · bas q05 -3.08%
   - session (n=160) : retour [-2.77% .. +2.52%] · haut q95 +3.37% · bas q05 -3.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 42.1  _(momentum baissier)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist -2.335  _(bearish_recent)_
- **BB** : %B 0.29 · largeur 10.7%
- **ATR** : 6.95 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.185  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 48.7  _(transition)_
- **MA** : MA20 351.54 · MA50 341.26 · MA200 309.32  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 +0.7% · MA200 +11.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (809209 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
