# SAF

**Generated** : 2026-07-15T00:07:15.366193+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €328.40  

> 🟡 **WAIT-FOR-DIP** — spot +2.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €328.40 (+2.9% vs entrée) · entrée €319.10 · stop €314.31 · T1 €322.59 · R/R 0.73  
> ↳ P(T1 av. stop) 57 % · EV/risk 0.07 · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €318.40–€319.80 (mid €319.10)
- Spot actuel : €328.40 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €314.31 (stop swing_plan-based (-7.38%))
- Targets : T1 €322.59 · R/R 0.73 | T2 €326.08 · R/R 1.46 | T3 €329.58 · R/R 2.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €314.31


## Edge, scénarios & sizing

- EV/risk : 0.07 | EV/share : €0.334 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 32 % | T3 13 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 10.3 | side 84.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


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

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 44.1  _(momentum baissier)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist -3.566  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 11.6%
- **ATR** : 8.93 (64.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.137  _(accumulation)_
- **Vol ratio** : 0.27  _(volume atone)_
- **Choppiness** : 44.4  _(transition)_
- **MA** : MA20 338.84 · MA50 310.44 · MA200 303.03  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 +5.8% · MA200 +8.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88109 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
