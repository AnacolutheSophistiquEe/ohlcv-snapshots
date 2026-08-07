# PRY

**Generated** : 2026-08-07T00:11:22.433259+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · €124.35  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €124.35 (+0.3% vs entrée) · entrée €123.97 · stop €114.06 · T1 €125.87 · R/R 0.19  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk -0.126 _(réel 5 s)_ (GBM -0.054) · ¼-Kelly 0.084 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €123.60–€124.35 (mid €123.97)
- Spot actuel : €124.35 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €114.06 (stop swing_plan-based (-5.83%))
- Targets : T1 €125.87 · R/R 0.19 | T2 €127.77 · R/R 0.38 | T3 €129.67 · R/R 0.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €114.06


## Edge, scénarios & sizing

- EV/risk : -0.054 | EV/share : €-0.534 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 27 % | T3 11 %
- Kelly (position) : f* 0.337 | ¼-Kelly 0.084 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 30.4 | bear 57.4 | side 12.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 249.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.304% → cible +1.531% / stop −8.0%, p_fill 89%, n_eff≈35.0) : P(cible|rempli) **38%** · **EV/risk -0.126** (×p_fill ; si rempli -1.14% du capital)
  - **swing** (entrée dip −0.597% → cible +3.424% / stop −5.264%, p_fill 84%, n_eff≈32.8) : P(cible|rempli) **30%** · **EV/risk -0.369** (×p_fill ; si rempli -2.32% du capital)
  - **deep** (entrée dip −0.87% → cible +4.842% / stop −7.919%, p_fill 96%, n_eff≈37.3) : P(cible|rempli) **27%** · **EV/risk -0.500** (×p_fill ; si rempli -4.15% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→39% · +3.0%→28% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.25% (p90 6.51%) · excursion haute méd. +1.37% / basse méd. −1.79%
- Profil de vol intra : ouverture 2.4% vs midi 0.853% vs clôture 1.197% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr 0.009)_ ; drift intra méd. -1.058% ; recovery-V 22%
- **σ réalisé intraday** 2.94% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 75% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 122.9355 (VA 122.2035–123.3015 ; dernier close 121.76)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=147) : méd. 0.35% · baisse 40% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=148) : bas méd −0.79% (p90 −2.39%) · haut méd +0.53% · range méd 1.5%
- Excursion ouverture 15min (n=148) : bas méd −0.94% (p90 −2.92%) · haut méd +0.67% · range méd 1.8%
- Excursion ouverture 30min (n=148) : bas méd −1.04% (p90 −3.21%) · haut méd +0.84% · range méd 1.99%
- Excursion ouverture 60min (n=148) : bas méd −1.23% (p90 −3.39%) · haut méd +0.89% · range méd 2.23%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 121.76 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 72% (107/147) · gap 27% · délai 0.2min · rebond 60% (67/107) (MFE +1.22%)
   - −1.0% : fill 30min 48% · séance 64% (91/147) · gap 20% · délai 0.3min · rebond 59% (55/91) (MFE +1.5%)
   - −1.5% : fill 30min 34% · séance 56% (79/147) · gap 16% · délai 1.9min · rebond 51% (43/79) (MFE +1.08%)
   - −2.0% : fill 30min 24% · séance 46% (64/147) · gap 11% · délai 13.0min · rebond 59% (40/64) (MFE +1.26%)
   - −3.0% : fill 30min 14% · séance 36% (47/147) · gap 4% · délai 76.9min · rebond 65% (32/47) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 21% (25/147) · gap 1% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 1% · séance 14% (17/147) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.75%) → stop au-delà de −1.5% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.3% (p90 −1.94%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −1.52%) → stop au-delà de −1.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=468 jambes) : jambe baissière méd −1.07% (p90 −2.62%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 90% (47/52) · rebond 46% (26/47)
      · −2.0% : fill 73% (38/52) · rebond 64% (26/38)
      · −3.0% : fill 60% (29/52) · rebond 71% (22/29)
      · −4.0% : fill 38% (16/52) · rebond 65% (11/16)
      · −5.0% : fill 29% (12/52) · rebond 73% (9/12)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (69 séances) :
      · −1.0% : fill 46% (30/69) · rebond 74% (20/30)
      · −2.0% : fill 30% (19/69) · rebond 43% (9/19)
      · −3.0% : fill 24% (13/69) · rebond 63% (8/13)
      · −4.0% : fill 13% (6/69) · rebond 86% (5/6)
      · −5.0% : fill 6% (3/69) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 46% en base · 70% si les 15 1res min sont vertes (69 cas) · 27% si rouges (79 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=148) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 83% si début vert vs 20% si rouge (base 46% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **83%** · continue >prix actuel 64% ; creux résiduel méd -1.32% (q20 -2.06%) → **SL/trailing à −2.06%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.41% / q75 +2.58% → **scale +1.41% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **20%** (continue à baisser 69%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-2.99% .. +2.79%] · haut q95 +3.56% · bas q05 -3.42%
   - 60min (n=148) : retour [-3.39% .. +2.23%] · haut q95 +4.0% · bas q05 -3.59%
   - 2h (n=148) : retour [-3.77% .. +2.67%] · haut q95 +4.1% · bas q05 -4.91%
   - 4h (n=148) : retour [-3.69% .. +3.23%] · haut q95 +4.47% · bas q05 -4.99%
   - 6h (n=148) : retour [-3.78% .. +3.72%] · haut q95 +4.74% · bas q05 -5.65%
   - session (n=148) : retour [-4.66% .. +4.58%] · haut q95 +5.73% · bas q05 -6.37%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.7% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.8  _(momentum baissier)_
- **ADX** : 34.8  _(tendance etablie)_
- **MACD** : hist 0.315  _(bullish_recent)_
- **BB** : %B 0.41 · largeur 20.9%
- **ATR** : 6.51 (95.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.015  _(neutre)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 56.7  _(transition)_
- **MA** : MA20 126.67 · MA50 138.27 · MA200 110.94  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -10.1% · MA200 +12.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93039 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
