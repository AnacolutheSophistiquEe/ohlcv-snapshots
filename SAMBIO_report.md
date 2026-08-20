# 207940

**Generated** : 2026-08-20T00:16:25.187213+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1544000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1544000.00 (+10.7% vs entrée) · entrée ₩1394675.00 · stop ₩1312334.45 · T1 ₩1559356.11 · R/R 2.0  
> ↳ P(T1 av. stop) 8 % · EV/risk -0.04 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1383532.74–₩1405817.26 (mid ₩1394675.00)
- Spot actuel : ₩1544000.00 (+10.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1312334.45 (stop swing_plan-based (-15.0%))
- Targets : T1 ₩1559356.11 · R/R 2.0 | T2 ₩1560329.26 · R/R 2.01 | T3 ₩1561302.40 · R/R 2.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1312334.45


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : ₩-3294.818 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 8 % | T2 7 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 53.7 | bear 33.5 | side 12.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=10, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→59% · +2.0%→40% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.08% (p90 6.65%) · excursion haute méd. +1.1% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.589% vs midi 0.758% vs clôture 0.85% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 11% · trend ↑1%/↓2% ; spike-down 57% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. 0.025% ; recovery-V 41%
- **σ réalisé intraday** 2.953% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 48% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 1549900.0 (VA 1548100.0–1552300.0 ; dernier close 1552000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 27% · rebond 57% · **stop −2.29%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.61 (high win-rate)
- Gaps overnight (n=154) : méd. 0.32% · baisse 31% (gap-down >1% 6% · >2% 3%)
- Excursion ouverture 5min (n=155) : bas méd −0.86% (p90 −2.44%) · haut méd +0.51% · range méd 1.49%
- Excursion ouverture 15min (n=155) : bas méd −1.07% (p90 −2.93%) · haut méd +0.69% · range méd 1.99%
- Excursion ouverture 30min (n=155) : bas méd −1.2% (p90 −3.28%) · haut méd +0.86% · range méd 2.39%
- Excursion ouverture 60min (n=155) : bas méd −1.27% (p90 −3.5%) · haut méd +0.92% · range méd 2.58%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1552000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 76% (106/154) · gap 17% · délai 1.1min · rebond 58% (50/106) (MFE +1.22%)
   - −1.0% : fill 30min 45% · séance 60% (83/154) · gap 6% · délai 3.0min · rebond 57% (38/83) (MFE +1.3%)
   - −1.5% : fill 30min 35% · séance 47% (64/154) · gap 4% · délai 3.5min · rebond 54% (30/64) (MFE +1.42%)
   - −2.0% : fill 30min 26% · séance 40% (55/154) · gap 3% · délai 7.1min · rebond 64% (30/55) (MFE +1.34%)
   - −3.0% : fill 30min 10% · séance 27% (35/154) · gap 1% · délai 87.0min · rebond 57% (19/35) (MFE +1.39%)
   - −4.0% : fill 30min 3% · séance 14% (18/154) · gap 1% · délai 73.5min · rebond 68% (11/18) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 7% (10/154) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.14%) → stop au-delà de −1.36% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.88% (p90 −2.06%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=398 jambes) : jambe baissière méd −1.1% (p90 −2.73%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (35 séances) :
      · −1.0% : fill 98% (34/35) · rebond 69% (18/34)
      · −2.0% : fill 84% (29/35) · rebond 68% (15/29)
      · −3.0% : fill 43% (15/35) · rebond 54% (8/15)
      · −4.0% : fill 31% (9/35) · rebond 76% (5/9)
      · −5.0% : fill 14% (5/35) · rebond 100% (5/5)
   - **flat** (46 séances) :
      · −1.0% : fill 53% (24/46) · rebond 27% (7/24)
      · −2.0% : fill 33% (11/46) · rebond 45% (5/11)
      · −3.0% : fill 27% (8/46) · rebond 73% (6/8)
      · −4.0% : fill 12% (4/46) · rebond 100% (4/4)
      · −5.0% : fill 5% (2/46) · rebond 89% (1/2)
   - **gap-up** (73 séances) :
      · −1.0% : fill 45% (25/73) · rebond 64% (13/25)
      · −2.0% : fill 23% (15/73) · rebond 72% (10/15)
      · −3.0% : fill 19% (12/73) · rebond 49% (5/12)
      · −4.0% : fill 8% (5/73) · rebond 33% (2/5)
      · −5.0% : fill 6% (3/73) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 44% en base · 64% si les 15 1res min sont vertes (55 cas) · 30% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=155) : COUDE à **28min** → P(séance verte=clôture>ouverture) 78% si début vert vs 26% si rouge (base 44% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=52) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.48% (q20 -2.53%) → **SL/trailing à −2.53%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +2.63% → **scale +1.64% / runner +2.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **26%** (continue à baisser 54%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.68%** (au-delà de la MAE q10 -3.68%), cible rebond +1.21% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-3.16% .. +3.31%] · haut q95 +3.68% · bas q05 -3.57%
   - 60min (n=155) : retour [-3.48% .. +2.75%] · haut q95 +4.01% · bas q05 -4.11%
   - 2h (n=155) : retour [-3.98% .. +3.42%] · haut q95 +4.47% · bas q05 -4.68%
   - 4h (n=155) : retour [-4.92% .. +3.67%] · haut q95 +5.07% · bas q05 -5.6%
   - 6h (n=155) : retour [-4.78% .. +4.01%] · haut q95 +5.1% · bas q05 -6.1%
   - session (n=155) : retour [-4.63% .. +3.61%] · haut q95 +5.1% · bas q05 -6.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.08%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 57.1  _(momentum haussier)_
- **ADX** : 14.5  _(pas de tendance nette)_
- **MACD** : hist -561.386  _(bearish_recent)_
- **BB** : %B 0.63 · largeur 16.4%
- **ATR** : 58000.0 (62.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.242  _(accumulation)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 49.1  _(transition)_
- **MA** : MA20 1511400.0 · MA50 1423660.0 · MA200 1601147.76  _(prix > MA20)_
- **Dist MA** : MA20 +2.2% · MA50 +8.5% · MA200 -3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (95462 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
