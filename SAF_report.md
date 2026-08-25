# SAF

**Generated** : 2026-08-25T00:07:29.597190+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €340.30  

> 🟡 **WAIT-FOR-DIP** — spot +3.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €340.30 (+3.6% vs entrée) · entrée €328.50 · stop €321.93 · T1 €331.20 · R/R 0.41  
> ↳ P(T1 av. stop) 52 % · EV/risk 0.017 · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €327.95–€329.04 (mid €328.50)
- Spot actuel : €340.30 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : €321.93 (stop swing_plan-based (-9.57%))
- Targets : T1 €331.20 · R/R 0.41 | T2 €333.91 · R/R 0.82 | T3 €336.62 · R/R 1.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €321.93


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.62 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (9.57 %)** : le gap seul le franchit 0.078 % des séances (1 fois sur 1280).
   - exécution **0.416 pt plus bas** dans le cas TYPIQUE (médiane), 0.416 au p90, **0.416 au pire**
   - perte réelle **9.986 %** en moyenne _(tirée par la queue)_, jusqu'à **9.986 %** — au lieu des 9.57 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0003 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.405 % | p01 -2.356 % | pire -9.986 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0119** [0.0025 ; 0.0371] _(largeur 3.5 pt, n_eff 173.1)_
   - swing : **0.1542** [0.1191 ; 0.1951] _(largeur 7.6 pt, n_eff 345.8)_
   - deep : **0.2499** [0.2065 ; 0.2975] _(largeur 9.1 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.19 %** | CVaR **-4.0 %** | vol 2.05 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 1.33 % contre 2.50 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.66 % vs -6.07 % si l'on extrapolait par √5 _(rapport 0.932 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3687** (β de hausse 1.3391, asymétrie 1.0221) vs FCHI — 616 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.264× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 304.0393 sur atr_grid (5.5 ATR, 10.656 %) — p(stop avant cible) 0.0709 [0.05 ; 0.10], R/R 0.589, perte reelle 10.656 % (gap inclus), CVaR 10.656 %, EV 1.0667 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - viole : R/R 0.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 2.906 %) — p(stop avant cible) 0.4639 [0.41 ; 0.52], R/R 1.365, perte reelle 4.602 % (gap inclus), EV 0.1175 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ sr_based a 7.26 ATR (stop 15.252 %) — p(stop avant cible) 0.0139 [0.01 ; 0.03], R/R 0.412, perte reelle 15.252 % (gap inclus), EV 1.0192 % — **REFUSE**
      - refuse : R/R 0.41 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.25 % > budget 12.00 %
   - 🟢 support a 12.23 ATR (stop 24.874 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.252, perte reelle 24.874 % (gap inclus), EV 1.0435 % — **REFUSE**
      - refuse : R/R 0.25 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.87 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 1.937 %) — p(stop avant cible) 0.6075 [0.56 ; 0.66], R/R 2.012, perte reelle 3.121 % (gap inclus), EV -0.0876 % — **REFUSE**
      - refuse : p_stop_first 0.608, borne haute 0.658 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 22.4 % x 6.28 % + P(rien) 16.8 % x 2.38 % ne couvrent pas P(stop) 60.8 % x 3.12 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.75 ATR (stop 3.39 %) — p(stop avant cible) 0.3997 [0.35 ; 0.45], R/R 1.102, perte reelle 5.698 % (gap inclus), EV 0.0641 % — **REFUSE**
      - refuse : R/R 1.10 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.0 ATR (stop 3.875 %) — p(stop avant cible) 0.3367 [0.29 ; 0.39], R/R 1.019, perte reelle 6.163 % (gap inclus), EV 0.3888 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.25 ATR (stop 4.359 %) — p(stop avant cible) 0.2976 [0.25 ; 0.35], R/R 0.924, perte reelle 6.799 % (gap inclus), EV 0.4017 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.5 ATR (stop 4.843 %) — p(stop avant cible) 0.2613 [0.22 ; 0.31], R/R 0.924, perte reelle 6.799 % (gap inclus), EV 0.7547 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 2.75 ATR (stop 5.328 %) — p(stop avant cible) 0.2328 [0.19 ; 0.28], R/R 0.817, perte reelle 7.683 % (gap inclus), EV 0.7139 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.0 ATR (stop 5.812 %) — p(stop avant cible) 0.2151 [0.17 ; 0.26], R/R 0.629, perte reelle 9.986 % (gap inclus), EV 0.4063 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 3.5 ATR (stop 6.781 %) — p(stop avant cible) 0.1725 [0.14 ; 0.21], R/R 0.629, perte reelle 9.986 % (gap inclus), EV 0.6794 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.0 ATR (stop 7.749 %) — p(stop avant cible) 0.1419 [0.11 ; 0.18], R/R 0.629, perte reelle 9.986 % (gap inclus), EV 0.8689 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 4.5 ATR (stop 8.718 %) — p(stop avant cible) 0.1207 [0.09 ; 0.16], R/R 0.629, perte reelle 9.986 % (gap inclus), EV 0.958 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.0 ATR (stop 9.687 %) — p(stop avant cible) 0.0867 [0.06 ; 0.12], R/R 0.629, perte reelle 9.986 % (gap inclus), EV 1.0571 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 5.5 ATR (stop 10.656 %) — p(stop avant cible) 0.0709 [0.05 ; 0.10], R/R 0.589, perte reelle 10.656 % (gap inclus), EV 1.0667 % — **REFUSE**
      - refuse : R/R 0.59 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.0 ATR (stop 11.624 %) — p(stop avant cible) 0.058 [0.04 ; 0.09], R/R 0.54, perte reelle 11.624 % (gap inclus), EV 1.035 % — **REFUSE**
      - refuse : R/R 0.54 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 6.5 ATR (stop 12.593 %) — p(stop avant cible) 0.0454 [0.03 ; 0.07], R/R 0.499, perte reelle 12.593 % (gap inclus), EV 1.0381 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.59 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 13.562 %) — p(stop avant cible) 0.0353 [0.02 ; 0.06], R/R 0.463, perte reelle 13.562 % (gap inclus), EV 1.0071 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.56 % > budget 12.00 %
   - ⚪ grid_snapped a 7.26 ATR (stop 14.649 %) — p(stop avant cible) 0.0206 [0.01 ; 0.04], R/R 0.429, perte reelle 14.649 % (gap inclus), EV 1.0102 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.65 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.017 | EV/share : €0.114 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 38 % | T3 19 %
- Kelly (position) : f* 0.111 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.0 | bear 56.9 | side 37.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
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

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 32.8  _(momentum baissier)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist -2.81  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 10.0%
- **ATR** : 6.59 (37.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.129  _(distribution)_
- **Vol ratio** : 0.31  _(volume atone)_
- **Choppiness** : 45.7  _(transition)_
- **MA** : MA20 351.89 · MA50 341.74 · MA200 309.53  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -0.4% · MA200 +9.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (802636 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
