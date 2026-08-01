# SAF

**Generated** : 2026-08-01T21:26:49.578645+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €339.50  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €339.50 (+8.1% vs entrée) · entrée €313.94 · stop €304.77 · T1 €320.85 · R/R 0.75  
> ↳ P(T1 av. stop) 48 % · EV/risk -0.03 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €312.56–€315.32 (mid €313.94)
- Spot actuel : €339.50 (+8.1% au-dessus de la zone — repli à attendre)
- Stop : €304.77 (stop swing_plan-based (-10.23%))
- Targets : T1 €320.85 · R/R 0.75 | T2 €327.76 · R/R 1.51 | T3 €334.67 · R/R 2.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €304.77


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : €-0.278 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 27 % | T3 16 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 32.5 | side 62.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 340.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=8, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→54% · +2.0%→34% · +3.0%→14% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.7% (p90 4.55%) · excursion haute méd. +1.13% / basse méd. −1.01%
- Profil de vol intra : ouverture 1.664% vs midi 0.62% vs clôture 0.744% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.102 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. 0.065% ; recovery-V 25%
- **σ réalisé intraday** 1.966% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 49% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 344.665 (VA 341.935–345.925 ; dernier close 339.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 18% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.01% · baisse 49% (gap-down >1% 10% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.5% (p90 −1.78%) · haut méd +0.18% · range méd 0.94%
- Excursion ouverture 15min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.31% · range méd 1.2%
- Excursion ouverture 30min (n=160) : bas méd −0.62% (p90 −1.93%) · haut méd +0.52% · range méd 1.35%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −1.98%) · haut méd +0.57% · range méd 1.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 339.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 69% (113/159) · gap 23% · délai 0.2min · rebond 38% (42/113) (MFE +0.78%)
   - −1.0% : fill 30min 43% · séance 54% (83/159) · gap 10% · délai 0.4min · rebond 41% (30/83) (MFE +0.63%)
   - −1.5% : fill 30min 30% · séance 46% (71/159) · gap 4% · délai 7.5min · rebond 45% (26/71) (MFE +0.91%)
   - −2.0% : fill 30min 14% · séance 35% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 18% (29/159) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 8% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.23% (p90 −0.91%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.16% (p90 −0.83%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=202 jambes) : jambe baissière méd −1.1% (p90 −2.51%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (44/55) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (46 séances) :
      · −1.0% : fill 48% (20/46) · rebond 56% (10/20)
      · −2.0% : fill 22% (9/46) · rebond 75% (5/9)
      · −3.0% : fill 11% (5/46) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/46) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/46) · rebond 0% (0/0)
   - **gap-up** (58 séances) :
      · −1.0% : fill 30% (19/58) · rebond 31% (4/19)
      · −2.0% : fill 19% (11/58) · rebond 43% (4/11)
      · −3.0% : fill 12% (7/58) · rebond 36% (4/7)
      · −4.0% : fill 5% (3/58) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/58) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 72% si les 15 1res min sont vertes (70 cas) · 34% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 81% si début vert vs 26% si rouge (base 52% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **81%** · continue >prix actuel 62% ; creux résiduel méd -0.57% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.78% → **scale +1.32% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **26%** (continue à baisser 49%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.44%** (au-delà de la MAE q10 -2.44%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.63% .. +1.57%] · haut q95 +1.96% · bas q05 -2.33%
   - 60min (n=160) : retour [-1.83% .. +2.12%] · haut q95 +2.19% · bas q05 -2.67%
   - 2h (n=160) : retour [-2.49% .. +2.14%] · haut q95 +2.54% · bas q05 -3.08%
   - 4h (n=160) : retour [-2.15% .. +2.19%] · haut q95 +2.98% · bas q05 -3.45%
   - 6h (n=160) : retour [-2.25% .. +2.91%] · haut q95 +3.27% · bas q05 -3.96%
   - session (n=160) : retour [-3.34% .. +2.87%] · haut q95 +3.65% · bas q05 -4.09%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.68%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist 0.236  _(bullish_recent)_
- **BB** : %B 0.65 · largeur 10.5%
- **ATR** : 9.17 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.024  _(neutre)_
- **Vol ratio** : 0.31  _(volume atone)_
- **Choppiness** : 54.3  _(transition)_
- **MA** : MA20 334.1 · MA50 323.99 · MA200 305.29  _(prix > MA20)_
- **Dist MA** : MA20 +1.6% · MA50 +4.8% · MA200 +11.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88008 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
