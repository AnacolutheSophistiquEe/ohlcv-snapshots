# 267260

**Generated** : 2026-08-03T00:13:55.216480+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩684000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩684000.00 (+2.4% vs entrée) · entrée ₩668090.15 · stop ₩614642.94 · T1 ₩740654.89 · R/R 1.36  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.082 _(réel 5 s)_ (GBM -0.181) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
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
- Stop : ₩614642.94 (stop swing_plan-based (-15.99%))
- Targets : T1 ₩740654.89 · R/R 1.36 | T2 ₩745931.32 · R/R 1.46 | T3 ₩751207.76 · R/R 1.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩614642.94


## Edge, scénarios & sizing

- EV/risk : -0.181 | EV/share : ₩-9693.988 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.019 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 66.0 | side 26.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.326% → cible +10.862% / stop −8.0%, p_fill 85%, n_eff≈34.0) : P(cible|rempli) **1%** · **EV/risk -0.082** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −5.119% → cible +9.273% / stop −11.457%, p_fill 62%, n_eff≈25.3) : P(cible|rempli) **29%** · **EV/risk -0.192** (×p_fill ; si rempli -3.57% du capital)
  - **deep** (entrée dip −7.903% → cible +13.114% / stop −17.707%, p_fill 71%, n_eff≈27.6) : P(cible|rempli) **39%** · **EV/risk -0.034** (×p_fill ; si rempli -0.86% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→46% · +3.0%→32% · +5.0%→12% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.58%) · excursion haute méd. +1.84% / basse méd. −3.88%
- Profil de vol intra : ouverture 4.329% vs midi 1.18% vs clôture 1.225% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; mean-reverting — autocorr -0.054)_ ; drift intra méd. -2.315% ; recovery-V 19%
- **σ réalisé intraday** 5.028% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 73% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 666262.5 (VA 664737.5–678462.5 ; dernier close 681000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 82% · **stop −5.38%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.38 (high win-rate)
- Gaps overnight (n=144) : méd. 1.12% · baisse 39% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=145) : bas méd −1.71% (p90 −4.35%) · haut méd +0.95% · range méd 2.85%
- Excursion ouverture 15min (n=145) : bas méd −1.95% (p90 −4.9%) · haut méd +1.06% · range méd 3.55%
- Excursion ouverture 30min (n=145) : bas méd −2.26% (p90 −5.19%) · haut méd +1.08% · range méd 3.83%
- Excursion ouverture 60min (n=145) : bas méd −2.92% (p90 −5.72%) · haut méd +1.26% · range méd 4.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 681000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (102/144) · gap 32% · délai 0.0min · rebond 51% (56/102) (MFE +1.07%)
   - −1.0% : fill 30min 55% · séance 69% (95/144) · gap 22% · délai 0.2min · rebond 56% (56/95) (MFE +1.25%)
   - −1.5% : fill 30min 48% · séance 63% (82/144) · gap 15% · délai 0.4min · rebond 65% (53/82) (MFE +1.27%)
   - −2.0% : fill 30min 43% · séance 58% (74/144) · gap 11% · délai 0.7min · rebond 68% (50/74) (MFE +1.61%)
   - −3.0% : fill 30min 34% · séance 50% (59/144) · gap 7% · délai 2.7min · rebond 77% (41/59) (MFE +1.92%)
   - −4.0% : fill 30min 25% · séance 42% (49/144) · gap 4% · délai 8.1min · rebond 74% (38/49) (MFE +2.29%)
   - −5.0% : fill 30min 17% · séance 36% (39/144) · gap 2% · délai 37.6min · rebond 82% (30/39) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.8%) → stop au-delà de −2.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −4.16%) → stop au-delà de −2.52% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.23% (p90 −5.23%) → stop au-delà de −3.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=736 jambes) : jambe baissière méd −1.31% (p90 −3.62%) · ~12.0 jambes/séance
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
   - **gap-up** (77 séances) :
      · −1.0% : fill 48% (32/77) · rebond 69% (23/32)
      · −2.0% : fill 33% (20/77) · rebond 74% (16/20)
      · −3.0% : fill 24% (12/77) · rebond 77% (9/12)
      · −4.0% : fill 19% (10/77) · rebond 82% (8/10)
      · −5.0% : fill 14% (7/77) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 33% en base · 50% si les 15 1res min sont vertes (66 cas) · 23% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=145) : COUDE à **57min** → P(séance verte=clôture>ouverture) 73% si début vert vs 11% si rouge (base 33% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **73%** · continue >prix actuel 46% ; creux résiduel méd -2.23% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.74% / q75 +2.87% → **scale +1.74% / runner +2.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **11%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.3%** (au-delà de la MAE q10 -6.3%), cible rebond +1.53% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-5.57% .. +2.7%] · haut q95 +4.27% · bas q05 -5.79%
   - 60min (n=145) : retour [-5.74% .. +3.07%] · haut q95 +4.48% · bas q05 -7.03%
   - 2h (n=145) : retour [-7.07% .. +3.7%] · haut q95 +5.26% · bas q05 -7.97%
   - 4h (n=145) : retour [-6.95% .. +4.11%] · haut q95 +5.44% · bas q05 -8.92%
   - 6h (n=145) : retour [-8.31% .. +4.48%] · haut q95 +6.91% · bas q05 -9.48%
   - session (n=145) : retour [-7.66% .. +4.77%] · haut q95 +6.99% · bas q05 -9.7%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.47%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82833 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
