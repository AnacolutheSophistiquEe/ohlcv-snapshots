# SAF

**Generated** : 2026-07-28T21:41:13.494535+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €343.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €343.00 (+8.9% vs entrée) · entrée €314.97 · stop €311.39 · T1 €322.13 · R/R 2.0  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.059 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 145 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €313.54–€316.40 (mid €314.97)
- Spot actuel : €343.00 (+8.9% au-dessus de la zone — repli à attendre)
- Stop : €311.39 (stop swing_plan-based (-9.22%))
- Targets : T1 €322.13 · R/R 2.0 | T2 €329.29 · R/R 4.0 | T3 €336.45 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €311.39


## Edge, scénarios & sizing

- EV/risk : 0.059 | EV/share : €0.212 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 17 % | T3 12 %
- Kelly (position) : f* 0.01 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 38.6 | side 56.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 343.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→54% · +2.0%→35% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.72% (p90 4.55%) · excursion haute méd. +1.13% / basse méd. −1.01%
- Profil de vol intra : ouverture 1.663% vs midi 0.625% vs clôture 0.746% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.056)_ ; drift intra méd. 0.144% ; recovery-V 28%
- **σ réalisé intraday** 1.839% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 49% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 337.4319 (VA 336.8806–339.4531 ; dernier close 335.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=157) : méd. -0.02% · baisse 51% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=158) : bas méd −0.5% (p90 −1.51%) · haut méd +0.18% · range méd 0.92%
- Excursion ouverture 15min (n=158) : bas méd −0.62% (p90 −1.66%) · haut méd +0.31% · range méd 1.18%
- Excursion ouverture 30min (n=158) : bas méd −0.62% (p90 −1.91%) · haut méd +0.47% · range méd 1.31%
- Excursion ouverture 60min (n=158) : bas méd −0.73% (p90 −1.92%) · haut méd +0.57% · range méd 1.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 335.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 68% (111/157) · gap 24% · délai 0.2min · rebond 38% (41/111) (MFE +0.78%)
   - −1.0% : fill 30min 43% · séance 54% (82/157) · gap 10% · délai 0.4min · rebond 39% (29/82) (MFE +0.62%)
   - −1.5% : fill 30min 29% · séance 46% (70/157) · gap 4% · délai 11.9min · rebond 43% (25/70) (MFE +0.9%)
   - −2.0% : fill 30min 15% · séance 37% (52/157) · gap 2% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 19% (29/157) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 8% (13/157) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/157) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −0.91%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.16% (p90 −0.83%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=192 jambes) : jambe baissière méd −1.1% (p90 −2.57%) · ~5.0 jambes/séance
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
   - **gap-up** (56 séances) :
      · −1.0% : fill 28% (18/56) · rebond 17% (3/18)
      · −2.0% : fill 21% (11/56) · rebond 43% (4/11)
      · −3.0% : fill 13% (7/56) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/56) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 54% en base · 75% si les 15 1res min sont vertes (69 cas) · 35% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=158) : COUDE à **44min** → P(séance verte=clôture>ouverture) 84% si début vert vs 27% si rouge (base 54% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **84%** · continue >prix actuel 64% ; creux résiduel méd -0.56% (q20 -1.4%) → **SL/trailing à −1.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.44% / q75 +1.85% → **scale +1.44% / runner +1.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **27%** (continue à baisser 51%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.44%** (au-delà de la MAE q10 -2.44%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-1.64% .. +1.57%] · haut q95 +1.97% · bas q05 -2.18%
   - 60min (n=158) : retour [-1.84% .. +2.13%] · haut q95 +2.25% · bas q05 -2.49%
   - 2h (n=158) : retour [-2.54% .. +2.15%] · haut q95 +2.54% · bas q05 -2.94%
   - 4h (n=158) : retour [-2.16% .. +2.19%] · haut q95 +3.03% · bas q05 -3.02%
   - 6h (n=158) : retour [-2.27% .. +2.91%] · haut q95 +3.32% · bas q05 -3.09%
   - session (n=158) : retour [-3.38% .. +3.14%] · haut q95 +3.65% · bas q05 -3.99%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 58.3  _(momentum haussier)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist -0.832  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 13.4%
- **ATR** : 9.21 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.126  _(accumulation)_
- **Vol ratio** : 1.24  _(volume normal)_
- **Choppiness** : 56.8  _(transition)_
- **MA** : MA20 336.12 · MA50 320.35 · MA200 304.64  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 +7.1% · MA200 +12.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88617 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
