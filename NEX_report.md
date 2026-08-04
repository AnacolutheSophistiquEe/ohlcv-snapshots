# NEX

**Generated** : 2026-08-04T00:08:06.398254+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €129.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €129.80 (+1.0% vs entrée) · entrée €128.50 · stop €118.22 · T1 €130.02 · R/R 0.15  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk -0.045 _(réel 5 s)_ (GBM -0.04) · ¼-Kelly 0.081 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €128.19–€128.80 (mid €128.50)
- Spot actuel : €129.80 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €118.22 (stop swing_plan-based (-5.8%))
- Targets : T1 €130.02 · R/R 0.15 | T2 €131.55 · R/R 0.3 | T3 €133.08 · R/R 0.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €118.22


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : €-0.411 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 23 % | T3 7 %
- Kelly (position) : f* 0.326 | ¼-Kelly 0.081 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.6 | bear 59.9 | side 29.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.0% → cible +1.189% / stop −8.0%, p_fill 62%, n_eff≈24.3) : P(cible|rempli) **33%** · **EV/risk -0.045** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −2.212% → cible +2.659% / stop −3.669%, p_fill 51%, n_eff≈21.8) : P(cible|rempli) **32%** · **EV/risk -0.196** (×p_fill ; si rempli -1.41% du capital)
  - **deep** (entrée dip −3.418% → cible +3.76% / stop −5.572%, p_fill 54%, n_eff≈21.8) : P(cible|rempli) **44%** · **EV/risk -0.085** (×p_fill ; si rempli -0.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→54% · +2.0%→28% · +3.0%→11% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.06% (p90 5.26%) · excursion haute méd. +1.07% / basse méd. −1.32%
- Profil de vol intra : ouverture 1.759% vs midi 0.554% vs clôture 0.769% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.041)_ ; drift intra méd. -0.716% ; recovery-V 12%
- **σ réalisé intraday** 2.2% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 75% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 134.7825 (VA 133.2075–135.2025 ; dernier close 132.1)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 54% · **stop −1.98%** sous le fill (sous le bruit) · cible +1.19% · R/R 0.6 (high win-rate)
- Gaps overnight (n=144) : méd. 0.14% · baisse 38% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=145) : bas méd −0.46% (p90 −2.04%) · haut méd +0.33% · range méd 1.05%
- Excursion ouverture 15min (n=145) : bas méd −0.59% (p90 −2.16%) · haut méd +0.44% · range méd 1.29%
- Excursion ouverture 30min (n=145) : bas méd −0.6% (p90 −2.28%) · haut méd +0.55% · range méd 1.41%
- Excursion ouverture 60min (n=145) : bas méd −0.78% (p90 −2.52%) · haut méd +0.6% · range méd 1.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 132.1 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 72% (103/144) · gap 23% · délai 0.4min · rebond 45% (50/103) (MFE +0.85%)
   - −1.0% : fill 30min 40% · séance 64% (86/144) · gap 10% · délai 9.4min · rebond 45% (40/86) (MFE +0.85%)
   - −1.5% : fill 30min 24% · séance 50% (64/144) · gap 3% · délai 60.6min · rebond 46% (30/64) (MFE +0.73%)
   - −2.0% : fill 30min 17% · séance 35% (48/144) · gap 2% · délai 70.9min · rebond 46% (25/48) (MFE +0.94%)
   - −3.0% : fill 30min 4% · séance 24% (30/144) · gap 1% · délai 126.4min · rebond 54% (17/30) (MFE +1.19%)
   - −4.0% : fill 30min 1% · séance 9% (11/144) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/144) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −1.11%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.08% (p90 −0.87%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=302 jambes) : jambe baissière méd −1.05% (p90 −2.47%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (35 séances) :
      · −1.0% : fill 75% (24/35) · rebond 49% (13/24)
      · −2.0% : fill 43% (12/35) · rebond 51% (6/12)
      · −3.0% : fill 32% (8/35) · rebond 46% (3/8)
      · −4.0% : fill 11% (2/35) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/35) · rebond 0% (0/0)
   - **gap-up** (65 séances) :
      · −1.0% : fill 46% (26/65) · rebond 41% (12/26)
      · −2.0% : fill 24% (11/65) · rebond 44% (6/11)
      · −3.0% : fill 14% (6/65) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/65) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/65) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 43% en base · 65% si les 15 1res min sont vertes (78 cas) · 18% si rouges (67 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=145) : COUDE à **28min** → P(séance verte=clôture>ouverture) 78% si début vert vs 17% si rouge (base 43% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 306min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -0.97% (q20 -1.94%) → **SL/trailing à −1.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.03% / q75 +1.71% → **scale +1.03% / runner +1.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **17%** (continue à baisser 57%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.23%** (au-delà de la MAE q10 -3.23%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-2.07% .. +2.24%] · haut q95 +2.45% · bas q05 -2.81%
   - 60min (n=145) : retour [-2.82% .. +2.18%] · haut q95 +2.75% · bas q05 -3.24%
   - 2h (n=145) : retour [-3.53% .. +2.15%] · haut q95 +2.93% · bas q05 -3.73%
   - 4h (n=145) : retour [-3.03% .. +2.37%] · haut q95 +2.94% · bas q05 -3.85%
   - 6h (n=145) : retour [-3.85% .. +3.32%] · haut q95 +3.73% · bas q05 -4.16%
   - session (n=145) : retour [-3.61% .. +2.86%] · haut q95 +4.08% · bas q05 -4.66%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 39.3  _(momentum baissier)_
- **ADX** : 33.9  _(tendance etablie)_
- **MACD** : hist 0.306  _(bullish_recent)_
- **BB** : %B 0.25 · largeur 8.5%
- **ATR** : 4.66 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.05  _(neutre)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 132.58 · MA50 143.7 · MA200 131.68  _(prix < MA20)_
- **Dist MA** : MA20 -2.1% · MA50 -9.7% · MA200 -1.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89669 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
