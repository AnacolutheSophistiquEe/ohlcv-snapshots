# SAF

**Generated** : 2026-07-21T21:41:13.016822+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €322.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €322.90 (+2.4% vs entrée) · entrée €315.18 · stop €308.88 · T1 €318.48 · R/R 0.52  
> ↳ P(T1 av. stop) 56 % · EV/risk 0.037 · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €314.52–€315.84 (mid €315.18)
- Spot actuel : €322.90 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : €308.88 (stop swing_plan-based (-6.37%))
- Targets : T1 €318.48 · R/R 0.52 | T2 €321.77 · R/R 1.05 | T3 €325.07 · R/R 1.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €308.88


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : €0.231 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 56 % | T2 34 % | T3 14 %
- Kelly (position) : f* 0.083 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 22.5 | side 72.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=15, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→56% · +2.0%→36% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.72% (p90 4.55%) · excursion haute méd. +1.33% / basse méd. −0.98%
- Profil de vol intra : ouverture 1.631% vs midi 0.624% vs clôture 0.745% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (153 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. 0.108% ; recovery-V 33%
- **σ réalisé intraday** 1.793% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 52% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 326.6725 (VA 325.8025–327.2525 ; dernier close 325.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=152) : méd. -0.06% · baisse 52% (gap-down >1% 11% · >2% 2%)
- Excursion ouverture 5min (n=153) : bas méd −0.48% (p90 −1.5%) · haut méd +0.21% · range méd 0.94%
- Excursion ouverture 15min (n=153) : bas méd −0.62% (p90 −1.61%) · haut méd +0.35% · range méd 1.2%
- Excursion ouverture 30min (n=153) : bas méd −0.62% (p90 −1.67%) · haut méd +0.44% · range méd 1.29%
- Excursion ouverture 60min (n=153) : bas méd −0.74% (p90 −1.82%) · haut méd +0.56% · range méd 1.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 325.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 68% (108/152) · gap 27% · délai 0.2min · rebond 38% (40/108) (MFE +0.76%)
   - −1.0% : fill 30min 45% · séance 55% (80/152) · gap 11% · délai 0.4min · rebond 42% (29/80) (MFE +0.67%)
   - −1.5% : fill 30min 30% · séance 47% (68/152) · gap 4% · délai 12.2min · rebond 42% (24/68) (MFE +0.9%)
   - −2.0% : fill 30min 14% · séance 36% (50/152) · gap 2% · délai 53.4min · rebond 47% (22/50) (MFE +0.87%)
   - −3.0% : fill 30min 4% · séance 19% (28/152) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 9% (13/152) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/152) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=185 jambes) : jambe baissière méd −1.07% (p90 −2.54%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (44/55) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (42 séances) :
      · −1.0% : fill 47% (18/42) · rebond 73% (10/18)
      · −2.0% : fill 14% (7/42) · rebond 50% (3/7)
      · −3.0% : fill 7% (4/42) · rebond 69% (3/4)
      · −4.0% : fill 1% (1/42) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/42) · rebond 0% (0/0)
   - **gap-up** (55 séances) :
      · −1.0% : fill 30% (18/55) · rebond 17% (3/18)
      · −2.0% : fill 22% (11/55) · rebond 43% (4/11)
      · −3.0% : fill 14% (7/55) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/55) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=153) : 53% en base · 72% si les 15 1res min sont vertes (67 cas) · 36% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=153) : COUDE à **44min** → P(séance verte=clôture>ouverture) 82% si début vert vs 29% si rouge (base 53% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **82%** · continue >prix actuel 64% ; creux résiduel méd -0.57% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.78% → **scale +1.32% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **29%** (continue à baisser 51%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.48%** (au-delà de la MAE q10 -2.48%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=153) : retour [-1.59% .. +1.58%] · haut q95 +1.94% · bas q05 -2.21%
   - 60min (n=153) : retour [-1.63% .. +2.14%] · haut q95 +2.63% · bas q05 -2.34%
   - 2h (n=153) : retour [-2.27% .. +2.18%] · haut q95 +2.65% · bas q05 -2.94%
   - 4h (n=153) : retour [-2.18% .. +2.19%] · haut q95 +3.24% · bas q05 -3.06%
   - 6h (n=153) : retour [-2.32% .. +2.91%] · haut q95 +3.43% · bas q05 -3.34%
   - session (n=153) : retour [-3.44% .. +3.28%] · haut q95 +3.67% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.0% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.6  _(survente)_
- **ADX** : 19.7  _(pas de tendance nette)_
- **MACD** : hist -3.845  _(pas de croisement recent)_
- **BB** : %B 0.14 · largeur 12.4%
- **ATR** : 8.79 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.225  _(accumulation)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 39.7  _(transition)_
- **MA** : MA20 338.2 · MA50 314.64 · MA200 303.78  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 +2.6% · MA200 +6.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88861 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
