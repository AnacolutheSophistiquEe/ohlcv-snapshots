# SAF

**Generated** : 2026-07-14T00:07:07.303324+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €328.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €328.90 (+6.7% vs entrée) · entrée €308.17 · stop €304.25 · T1 €316.01 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.11 · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €306.60–€309.74 (mid €308.17)
- Spot actuel : €328.90 (+6.7% au-dessus de la zone — repli à attendre)
- Stop : €304.25 (stop swing_plan-based (-7.5%))
- Targets : T1 €316.01 · R/R 2.0 | T2 €323.85 · R/R 4.0 | T3 €331.69 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €304.25


## Edge, scénarios & sizing

- EV/risk : 0.11 | EV/share : €0.429 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 16 % | T3 11 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 11.4 | side 83.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 329.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→60% · +2.0%→39% · +3.0%→16% · +5.0%→5% · +8.0%→2%
- Range intraday médian 2.75% (p90 4.62%) · excursion haute méd. +1.61% / basse méd. −0.92%
- Profil de vol intra : ouverture 1.637% vs midi 0.641% vs clôture 0.757% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (147 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 19% · trend ↑0%/↓0% ; spike-down 35% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. 0.286% ; recovery-V 18%
- **σ réalisé intraday** 1.766% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 54% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 337.4362 (VA 336.5238–338.7138 ; dernier close 336.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 21% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=146) : méd. -0.06% · baisse 52% (gap-down >1% 12% · >2% 2%)
- Excursion ouverture 5min (n=147) : bas méd −0.36% (p90 −1.53%) · haut méd +0.27% · range méd 0.91%
- Excursion ouverture 15min (n=147) : bas méd −0.38% (p90 −1.68%) · haut méd +0.48% · range méd 1.17%
- Excursion ouverture 30min (n=147) : bas méd −0.46% (p90 −1.91%) · haut méd +0.57% · range méd 1.28%
- Excursion ouverture 60min (n=147) : bas méd −0.67% (p90 −1.92%) · haut méd +0.69% · range méd 1.47%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 336.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 65% (102/146) · gap 28% · délai 0.2min · rebond 36% (37/102) (MFE +0.65%)
   - −1.0% : fill 30min 40% · séance 50% (74/146) · gap 12% · délai 0.4min · rebond 40% (26/74) (MFE +0.58%)
   - −1.5% : fill 30min 26% · séance 42% (63/146) · gap 4% · délai 7.6min · rebond 33% (20/63) (MFE +0.81%)
   - −2.0% : fill 30min 14% · séance 33% (46/146) · gap 2% · délai 54.7min · rebond 40% (19/46) (MFE +0.74%)
   - −3.0% : fill 30min 4% · séance 21% (28/146) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 10% (13/146) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 2% (3/146) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=171 jambes) : jambe baissière méd −1.07% (p90 −2.69%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 79% (41/52) · rebond 38% (15/41)
      · −2.0% : fill 57% (29/52) · rebond 43% (13/29)
      · −3.0% : fill 35% (17/52) · rebond 50% (9/17)
      · −4.0% : fill 18% (9/52) · rebond 69% (5/9)
      · −5.0% : fill 3% (2/52) · rebond 0% (0/2)
   - **flat** (40 séances) :
      · −1.0% : fill 39% (16/40) · rebond 62% (8/16)
      · −2.0% : fill 17% (7/40) · rebond 50% (3/7)
      · −3.0% : fill 8% (4/40) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/40) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/40) · rebond 0% (0/0)
   - **gap-up** (54 séances) :
      · −1.0% : fill 26% (17/54) · rebond 21% (3/17)
      · −2.0% : fill 18% (10/54) · rebond 24% (3/10)
      · −3.0% : fill 15% (7/54) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/54) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=147) : 54% en base · 72% si les 15 1res min sont vertes (67 cas) · 32% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=147) : COUDE à **44min** → P(séance verte=clôture>ouverture) 82% si début vert vs 24% si rouge (base 54% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **82%** · continue >prix actuel 64% ; creux résiduel méd -0.57% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.78% → **scale +1.32% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **24%** (continue à baisser 51%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.77%** (au-delà de la MAE q10 -2.77%), cible rebond +0.85% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=147) : retour [-1.62% .. +1.58%] · haut q95 +1.97% · bas q05 -2.26%
   - 60min (n=147) : retour [-1.7% .. +2.21%] · haut q95 +2.77% · bas q05 -2.42%
   - 2h (n=147) : retour [-2.4% .. +2.23%] · haut q95 +3.16% · bas q05 -2.99%
   - 4h (n=147) : retour [-2.39% .. +2.27%] · haut q95 +3.4% · bas q05 -3.3%
   - 6h (n=147) : retour [-2.35% .. +3.19%] · haut q95 +3.55% · bas q05 -3.53%
   - session (n=147) : retour [-3.49% .. +3.44%] · haut q95 +3.87% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.0% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.8  _(neutre)_
- **ADX** : 27.0  _(tendance etablie)_
- **MACD** : hist -3.069  _(bearish_recent)_
- **BB** : %B 0.26 · largeur 12.1%
- **ATR** : 9.01 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.151  _(accumulation)_
- **Vol ratio** : 0.23  _(volume atone)_
- **Choppiness** : 50.7  _(transition)_
- **MA** : MA20 338.56 · MA50 309.24 · MA200 302.85  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 +6.4% · MA200 +8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91023 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
