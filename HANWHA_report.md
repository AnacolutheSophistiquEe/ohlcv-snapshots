# 012450

**Generated** : 2026-07-22T00:17:49.005256+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩899000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩899000.00 (+2.7% vs entrée) · entrée ₩875120.69 · stop ₩805111.04 · T1 ₩899702.30 · R/R 0.35  
> ↳ P(T1 av. stop) 44 % _(réel 5 s)_ · EV/risk -0.025 _(réel 5 s)_ (GBM -0.146) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩870302.17–₩879939.21 (mid ₩875120.69)
- Spot actuel : ₩899000.00 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : ₩805111.04 (stop swing_plan-based (-8.91%))
- Targets : T1 ₩899702.30 · R/R 0.35 | T2 ₩923440.90 · R/R 0.69 | T3 ₩947179.50 · R/R 1.03
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩805111.04


## Edge, scénarios & sizing

- EV/risk : -0.146 | EV/share : ₩-10253.491 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.113 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.3 | bear 74.0 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.652% → cible +2.809% / stop −8.0%, p_fill 74%, n_eff≈27.6) : P(cible|rempli) **44%** · **EV/risk -0.025** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −5.847% → cible +6.137% / stop −3.253%, p_fill 54%, n_eff≈19.6) : P(cible|rempli) **29%** · **EV/risk -0.115** (×p_fill ; si rempli -0.70% du capital)
  - **deep** (entrée dip −9.032% → cible +8.68% / stop −4.34%, p_fill 43%, n_eff≈15.1) : P(cible|rempli) **15%** · **EV/risk -0.244** (×p_fill ; si rempli -2.45% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→59% · +2.0%→40% · +3.0%→24% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.75% (p90 8.37%) · excursion haute méd. +1.72% / basse méd. −3.17%
- Profil de vol intra : ouverture 4.073% vs midi 1.089% vs clôture 1.142% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓1% ; spike-down 88% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; mean-reverting — autocorr -0.072)_ ; drift intra méd. -1.921% ; recovery-V 29%
- **σ réalisé intraday** 4.655% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 38% / bas 64% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 909650.0 (VA 881050.0–921350.0 ; dernier close 874000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 83% · **stop −4.03%** sous le fill (sous le bruit) · cible +2.46% · R/R 0.61 (high win-rate)
- Gaps overnight (n=139) : méd. 0.78% · baisse 30% (gap-down >1% 18% · >2% 7%)
- Excursion ouverture 5min (n=140) : bas méd −1.83% (p90 −4.05%) · haut méd +0.79% · range méd 2.82%
- Excursion ouverture 15min (n=140) : bas méd −2.14% (p90 −4.65%) · haut méd +0.99% · range méd 3.4%
- Excursion ouverture 30min (n=140) : bas méd −2.34% (p90 −5.06%) · haut méd +1.08% · range méd 3.95%
- Excursion ouverture 60min (n=140) : bas méd −2.56% (p90 −5.52%) · haut méd +1.28% · range méd 4.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 874000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 75% (101/139) · gap 22% · délai 0.2min · rebond 50% (51/101) (MFE +0.92%)
   - −1.0% : fill 30min 58% · séance 73% (98/139) · gap 18% · délai 1.0min · rebond 55% (58/98) (MFE +1.01%)
   - −1.5% : fill 30min 55% · séance 69% (91/139) · gap 10% · délai 1.7min · rebond 59% (52/91) (MFE +1.26%)
   - −2.0% : fill 30min 46% · séance 60% (75/139) · gap 7% · délai 4.0min · rebond 64% (46/75) (MFE +1.55%)
   - −3.0% : fill 30min 31% · séance 49% (55/139) · gap 3% · délai 7.1min · rebond 72% (38/55) (MFE +1.54%)
   - −4.0% : fill 30min 22% · séance 36% (41/139) · gap 2% · délai 14.0min · rebond 84% (34/41) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 26% (30/139) · gap 1% · délai 41.9min · rebond 83% (25/30) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.21%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.41% (p90 −2.89%) → stop au-delà de −2.67% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.67% (p90 −2.86%) → stop au-delà de −2.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=654 jambes) : jambe baissière méd −1.29% (p90 −3.23%) · ~11.0 jambes/séance
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
   - **gap-up** (91 séances) :
      · −1.0% : fill 57% (50/91) · rebond 64% (35/50)
      · −2.0% : fill 42% (33/91) · rebond 70% (23/33)
      · −3.0% : fill 30% (22/91) · rebond 86% (18/22)
      · −4.0% : fill 16% (11/91) · rebond 100% (11/11)
      · −5.0% : fill 10% (8/91) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 32% en base · 59% si les 15 1res min sont vertes (46 cas) · 17% si rouges (94 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=140) : COUDE à **51min** → P(séance verte=clôture>ouverture) 81% si début vert vs 7% si rouge (base 32% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=46) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -2.3% (q20 -3.35%) → **SL/trailing à −3.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +3.4% → **scale +1.8% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=94) : edge inversé — récupère vert seulement **7%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.07%** (au-delà de la MAE q10 -5.07%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-5.54% .. +3.93%] · haut q95 +5.54% · bas q05 -6.78%
   - 60min (n=140) : retour [-5.22% .. +3.63%] · haut q95 +6.11% · bas q05 -7.2%
   - 2h (n=140) : retour [-6.97% .. +3.71%] · haut q95 +6.11% · bas q05 -8.06%
   - 4h (n=140) : retour [-6.7% .. +5.52%] · haut q95 +6.97% · bas q05 -8.47%
   - 6h (n=140) : retour [-6.82% .. +4.19%] · haut q95 +7.12% · bas q05 -8.46%
   - session (n=140) : retour [-6.89% .. +4.63%] · haut q95 +7.12% · bas q05 -8.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.9  _(momentum baissier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist -12047.971  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 36.7%
- **ATR** : 91785.71 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.137  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 45.8  _(transition)_
- **MA** : MA20 1017000.0 · MA50 1111800.0 · MA200 1144911.68  _(prix < MA20)_
- **Dist MA** : MA20 -11.6% · MA50 -19.1% · MA200 -21.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82661 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
