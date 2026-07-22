# 012450

**Generated** : 2026-07-22T21:53:33.661727+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩891000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩891000.00 (+2.5% vs entrée) · entrée ₩869120.69 · stop ₩799591.04 · T1 ₩899702.30 · R/R 0.44  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.051 _(réel 5 s)_ (GBM -0.142) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩864404.70–₩873836.69 (mid ₩869120.69)
- Spot actuel : ₩891000.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : ₩799591.04 (stop swing_plan-based (-8.31%))
- Targets : T1 ₩899702.30 · R/R 0.44 | T2 ₩919674.26 · R/R 0.73 | T3 ₩939646.23 · R/R 1.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩799591.04


## Edge, scénarios & sizing

- EV/risk : -0.142 | EV/share : ₩-9904.079 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 22 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.096 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.1 | bear 74.0 | side 8.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.457% → cible +3.519% / stop −8.0%, p_fill 77%, n_eff≈29.5) : P(cible|rempli) **31%** · **EV/risk -0.051** (×p_fill ; si rempli -0.53% du capital)
  - **swing** (entrée dip −5.397% → cible +6.048% / stop −3.079%, p_fill 55%, n_eff≈20.7) : P(cible|rempli) **16%** · **EV/risk -0.284** (×p_fill ; si rempli -1.60% du capital)
  - **deep** (entrée dip −8.35% → cible +8.554% / stop −4.277%, p_fill 53%, n_eff≈18.4) : P(cible|rempli) **16%** · **EV/risk -0.301** (×p_fill ; si rempli -2.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→59% · +2.0%→40% · +3.0%→25% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.84% (p90 8.37%) · excursion haute méd. +1.72% / basse méd. −3.04%
- Profil de vol intra : ouverture 4.071% vs midi 1.099% vs clôture 1.136% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑0%/↓1% ; spike-down 88% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. -1.769% ; recovery-V 32%
- **σ réalisé intraday** 4.637% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 61% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 899750.0 (VA 895250.0–905750.0 ; dernier close 891000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 83% · **stop −4.03%** sous le fill (sous le bruit) · cible +2.46% · R/R 0.61 (high win-rate)
- Gaps overnight (n=140) : méd. 0.71% · baisse 30% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=141) : bas méd −1.83% (p90 −4.05%) · haut méd +0.77% · range méd 2.83%
- Excursion ouverture 15min (n=141) : bas méd −2.15% (p90 −4.64%) · haut méd +0.98% · range méd 3.38%
- Excursion ouverture 30min (n=141) : bas méd −2.51% (p90 −5.03%) · haut méd +1.02% · range méd 3.91%
- Excursion ouverture 60min (n=141) : bas méd −2.6% (p90 −5.47%) · haut méd +1.28% · range méd 4.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 891000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 76% (102/140) · gap 22% · délai 0.2min · rebond 51% (52/102) (MFE +1.05%)
   - −1.0% : fill 30min 59% · séance 74% (99/140) · gap 18% · délai 1.1min · rebond 56% (59/99) (MFE +1.08%)
   - −1.5% : fill 30min 56% · séance 69% (92/140) · gap 10% · délai 1.7min · rebond 60% (53/92) (MFE +1.35%)
   - −2.0% : fill 30min 47% · séance 61% (76/140) · gap 7% · délai 3.6min · rebond 65% (47/76) (MFE +1.63%)
   - −3.0% : fill 30min 31% · séance 48% (55/140) · gap 3% · délai 7.1min · rebond 72% (38/55) (MFE +1.54%)
   - −4.0% : fill 30min 22% · séance 35% (41/140) · gap 2% · délai 14.0min · rebond 84% (34/41) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 26% (30/140) · gap 1% · délai 41.9min · rebond 83% (25/30) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.62%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.59% (p90 −2.88%) → stop au-delà de −2.65% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.79% (p90 −2.83%) → stop au-delà de −2.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=660 jambes) : jambe baissière méd −1.29% (p90 −3.21%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 100% (31/31) · rebond 47% (14/31)
      · −2.0% : fill 93% (28/31) · rebond 61% (16/28)
      · −3.0% : fill 88% (25/31) · rebond 70% (17/25)
      · −4.0% : fill 73% (22/31) · rebond 87% (18/22)
      · −5.0% : fill 50% (15/31) · rebond 85% (13/15)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 48% (9/17)
      · −2.0% : fill 87% (14/17) · rebond 56% (7/14)
      · −3.0% : fill 63% (8/17) · rebond 46% (3/8)
      · −4.0% : fill 63% (8/17) · rebond 60% (5/8)
      · −5.0% : fill 60% (7/17) · rebond 66% (4/7)
   - **gap-up** (92 séances) :
      · −1.0% : fill 58% (51/92) · rebond 66% (36/51)
      · −2.0% : fill 44% (34/92) · rebond 72% (24/34)
      · −3.0% : fill 29% (22/92) · rebond 86% (18/22)
      · −4.0% : fill 15% (11/92) · rebond 100% (11/11)
      · −5.0% : fill 10% (8/92) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 33% en base · 59% si les 15 1res min sont vertes (46 cas) · 19% si rouges (95 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=141) : COUDE à **51min** → P(séance verte=clôture>ouverture) 82% si début vert vs 7% si rouge (base 33% · écart 75 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=47) : tient le vert **82%** · continue >prix actuel 55% ; creux résiduel méd -2.07% (q20 -3.28%) → **SL/trailing à −3.28%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.95% / q75 +3.28% → **scale +1.95% / runner +3.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **7%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.07%** (au-delà de la MAE q10 -5.07%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-5.47% .. +3.91%] · haut q95 +5.52% · bas q05 -6.69%
   - 60min (n=141) : retour [-5.2% .. +3.46%] · haut q95 +6.06% · bas q05 -7.17%
   - 2h (n=141) : retour [-6.94% .. +3.7%] · haut q95 +6.06% · bas q05 -8.04%
   - 4h (n=141) : retour [-6.64% .. +5.51%] · haut q95 +6.94% · bas q05 -8.42%
   - 6h (n=141) : retour [-6.81% .. +4.18%] · haut q95 +7.11% · bas q05 -8.44%
   - session (n=141) : retour [-6.86% .. +4.5%] · haut q95 +7.11% · bas q05 -8.44%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.45%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 32.9  _(momentum baissier)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist -10391.339  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 38.3%
- **ATR** : 86500.0 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.147  _(distribution)_
- **Vol ratio** : 0.86  _(volume normal)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 1007900.0 · MA50 1103480.0 · MA200 1144297.8  _(prix < MA20)_
- **Dist MA** : MA20 -11.6% · MA50 -19.3% · MA200 -22.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82664 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
