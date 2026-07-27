# SAF

**Generated** : 2026-07-27T00:06:31.569669+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €329.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €329.80 (+2.9% vs entrée) · entrée €320.36 · stop €294.73 · T1 €323.57 · R/R 0.13  
> ↳ P(T1 av. stop) 54 % · EV/risk -0.013 · ¼-Kelly 0.101 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €319.72–€321.00 (mid €320.36)
- Spot actuel : €329.80 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €294.73 (stop swing_plan-based (-7.35%))
- Targets : T1 €323.57 · R/R 0.13 | T2 €326.77 · R/R 0.25 | T3 €329.98 · R/R 0.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €294.73


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.335 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 35 % | T3 15 %
- Kelly (position) : f* 0.403 | ¼-Kelly 0.101 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 22.7 | side 72.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=15, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→54% · +2.0%→35% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.75% (p90 4.55%) · excursion haute méd. +1.13% / basse méd. −1.01%
- Profil de vol intra : ouverture 1.649% vs midi 0.624% vs clôture 0.748% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.039)_ ; drift intra méd. 0.149% ; recovery-V 28%
- **σ réalisé intraday** 1.8% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 52% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 327.735 (VA 324.765–328.815 ; dernier close 330.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=156) : méd. -0.04% · baisse 52% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=157) : bas méd −0.51% (p90 −1.55%) · haut méd +0.14% · range méd 0.92%
- Excursion ouverture 15min (n=157) : bas méd −0.62% (p90 −1.71%) · haut méd +0.26% · range méd 1.17%
- Excursion ouverture 30min (n=157) : bas méd −0.64% (p90 −1.91%) · haut méd +0.44% · range méd 1.3%
- Excursion ouverture 60min (n=157) : bas méd −0.74% (p90 −1.92%) · haut méd +0.56% · range méd 1.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 330.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 69% (111/156) · gap 25% · délai 0.2min · rebond 38% (41/111) (MFE +0.78%)
   - −1.0% : fill 30min 44% · séance 55% (82/156) · gap 10% · délai 0.4min · rebond 39% (29/82) (MFE +0.62%)
   - −1.5% : fill 30min 30% · séance 47% (70/156) · gap 4% · délai 11.9min · rebond 43% (25/70) (MFE +0.9%)
   - −2.0% : fill 30min 15% · séance 38% (52/156) · gap 2% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 4% · séance 19% (29/156) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 8% (13/156) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/156) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.28% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −0.88%) → stop au-delà de −0.67% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=190 jambes) : jambe baissière méd −1.1% (p90 −2.59%) · ~5.0 jambes/séance
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
   - **gap-up** (55 séances) :
      · −1.0% : fill 30% (18/55) · rebond 17% (3/18)
      · −2.0% : fill 22% (11/55) · rebond 43% (4/11)
      · −3.0% : fill 14% (7/55) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/55) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 53% en base · 74% si les 15 1res min sont vertes (68 cas) · 35% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=157) : COUDE à **44min** → P(séance verte=clôture>ouverture) 83% si début vert vs 27% si rouge (base 53% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **83%** · continue >prix actuel 67% ; creux résiduel méd -0.53% (q20 -1.4%) → **SL/trailing à −1.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.94% → **scale +1.32% / runner +1.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **27%** (continue à baisser 51%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.44%** (au-delà de la MAE q10 -2.44%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-1.64% .. +1.57%] · haut q95 +1.93% · bas q05 -2.19%
   - 60min (n=157) : retour [-1.84% .. +2.13%] · haut q95 +2.28% · bas q05 -2.49%
   - 2h (n=157) : retour [-2.56% .. +2.15%] · haut q95 +2.54% · bas q05 -2.94%
   - 4h (n=157) : retour [-2.16% .. +2.19%] · haut q95 +3.07% · bas q05 -3.03%
   - 6h (n=157) : retour [-2.28% .. +2.91%] · haut q95 +3.34% · bas q05 -3.13%
   - session (n=157) : retour [-3.39% .. +3.28%] · haut q95 +3.65% · bas q05 -4.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.7  _(momentum baissier)_
- **ADX** : 18.3  _(pas de tendance nette)_
- **MACD** : hist -2.766  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 13.5%
- **ATR** : 9.17 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.251  _(accumulation)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 44.5  _(transition)_
- **MA** : MA20 336.38 · MA50 317.67 · MA200 304.2  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 +3.8% · MA200 +8.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88105 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
