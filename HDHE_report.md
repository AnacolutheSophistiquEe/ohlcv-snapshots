# 267260

**Generated** : 2026-07-31T21:51:14.878166+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩684000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩684000.00 (+2.4% vs entrée) · entrée ₩668090.15 · stop ₩614642.94 · T1 ₩740654.89 · R/R 1.36  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.106 _(réel 5 s)_ (GBM -0.192) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩662532.13–₩673648.16 (mid ₩668090.15)
- Spot actuel : ₩684000.00 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : ₩614642.94 (stop swing_plan-based (-9.52%))
- Targets : T1 ₩740654.89 · R/R 1.36 | T2 ₩745931.32 · R/R 1.46 | T3 ₩751207.76 · R/R 1.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩614642.94


## Edge, scénarios & sizing

- EV/risk : -0.192 | EV/share : ₩-10275.227 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 11 % | T3 11 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 66.0 | side 26.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.326% → cible +10.862% / stop −8.0%, p_fill 83%, n_eff≈33.6) : P(cible|rempli) **1%** · **EV/risk -0.106** (×p_fill ; si rempli -1.02% du capital)
  - **swing** (entrée dip −5.121% → cible +9.273% / stop −4.637%, p_fill 58%, n_eff≈25.4) : P(cible|rempli) **18%** · **EV/risk -0.281** (×p_fill ; si rempli -2.25% du capital)
  - **deep** (entrée dip −7.912% → cible +13.114% / stop −6.557%, p_fill 73%, n_eff≈27.3) : P(cible|rempli) **28%** · **EV/risk -0.163** (×p_fill ; si rempli -1.47% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→68% · +2.0%→45% · +3.0%→30% · +5.0%→11% · +8.0%→5%
- Range intraday médian 6.71% (p90 10.58%) · excursion haute méd. +1.77% / basse méd. −3.73%
- Profil de vol intra : ouverture 4.217% vs midi 1.124% vs clôture 1.2% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.043)_ ; drift intra méd. -2.516% ; recovery-V 16%
- **σ réalisé intraday** 4.912% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 75% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 573487.5 (VA 560962.5–611062.5 ; dernier close 579000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 38% · rebond 82% · **stop −5.38%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.38 (high win-rate)
- Gaps overnight (n=142) : méd. 0.55% · baisse 41% (gap-down >1% 23% · >2% 11%)
- Excursion ouverture 5min (n=143) : bas méd −1.67% (p90 −4.02%) · haut méd +0.92% · range méd 2.71%
- Excursion ouverture 15min (n=143) : bas méd −1.95% (p90 −4.69%) · haut méd +1.05% · range méd 3.42%
- Excursion ouverture 30min (n=143) : bas méd −2.26% (p90 −5.09%) · haut méd +1.06% · range méd 3.79%
- Excursion ouverture 60min (n=143) : bas méd −2.92% (p90 −5.73%) · haut méd +1.12% · range méd 4.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 579000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 72% (101/142) · gap 34% · délai 0.0min · rebond 50% (55/101) (MFE +0.97%)
   - −1.0% : fill 30min 57% · séance 70% (94/142) · gap 23% · délai 0.2min · rebond 55% (55/94) (MFE +1.16%)
   - −1.5% : fill 30min 50% · séance 64% (81/142) · gap 16% · délai 0.4min · rebond 64% (52/81) (MFE +1.26%)
   - −2.0% : fill 30min 45% · séance 60% (74/142) · gap 11% · délai 0.7min · rebond 68% (50/74) (MFE +1.61%)
   - −3.0% : fill 30min 35% · séance 52% (59/142) · gap 8% · délai 2.7min · rebond 77% (41/59) (MFE +1.92%)
   - −4.0% : fill 30min 26% · séance 44% (49/142) · gap 4% · délai 8.1min · rebond 74% (38/49) (MFE +2.29%)
   - −5.0% : fill 30min 17% · séance 38% (39/142) · gap 2% · délai 37.6min · rebond 82% (30/39) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.41%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.31%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −4.6%) → stop au-delà de −3.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=718 jambes) : jambe baissière méd −1.29% (p90 −3.71%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (50 séances) :
      · −1.0% : fill 98% (49/50) · rebond 49% (26/49)
      · −2.0% : fill 93% (42/50) · rebond 61% (25/42)
      · −3.0% : fill 84% (36/50) · rebond 75% (24/36)
      · −4.0% : fill 76% (32/50) · rebond 73% (25/32)
      · −5.0% : fill 66% (25/50) · rebond 80% (19/25)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (75 séances) :
      · −1.0% : fill 48% (31/75) · rebond 66% (22/31)
      · −2.0% : fill 35% (20/75) · rebond 74% (16/20)
      · −3.0% : fill 26% (12/75) · rebond 77% (9/12)
      · −4.0% : fill 21% (10/75) · rebond 82% (8/10)
      · −5.0% : fill 14% (7/75) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 32% en base · 50% si les 15 1res min sont vertes (66 cas) · 21% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=143) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 74% si début vert vs 9% si rouge (base 32% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **74%** · continue >prix actuel 45% ; creux résiduel méd -1.47% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +2.7% → **scale +1.23% / runner +2.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **9%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-5.63% .. +2.68%] · haut q95 +4.29% · bas q05 -5.79%
   - 60min (n=143) : retour [-5.77% .. +3.13%] · haut q95 +4.5% · bas q05 -7.26%
   - 2h (n=143) : retour [-7.2% .. +3.66%] · haut q95 +5.01% · bas q05 -8.07%
   - 4h (n=143) : retour [-6.95% .. +4.29%] · haut q95 +5.46% · bas q05 -9.05%
   - 6h (n=143) : retour [-8.35% .. +4.53%] · haut q95 +7.07% · bas q05 -9.52%
   - session (n=143) : retour [-7.67% .. +5.05%] · haut q95 +7.13% · bas q05 -9.71%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.45%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 37.6  _(momentum baissier)_
- **ADX** : 29.2  _(tendance etablie)_
- **MACD** : hist -11848.236  _(bearish_recent)_
- **BB** : %B 0.22 · largeur 48.2%
- **ATR** : 74357.14 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.109  _(distribution)_
- **Vol ratio** : 1.33  _(volume normal)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 790850.0 · MA50 935340.0 · MA200 922027.02  _(prix < MA20)_
- **Dist MA** : MA20 -13.5% · MA50 -26.9% · MA200 -25.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83069 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
