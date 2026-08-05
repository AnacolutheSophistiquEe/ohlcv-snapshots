# NEX

**Generated** : 2026-08-05T00:08:10.291592+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €132.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €132.70 (+1.6% vs entrée) · entrée €130.67 · stop €120.22 · T1 €132.30 · R/R 0.16  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.031 _(réel 5 s)_ (GBM -0.041) · ¼-Kelly 0.078 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €130.35–€131.00 (mid €130.67)
- Spot actuel : €132.70 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €120.22 (stop swing_plan-based (-6.88%))
- Targets : T1 €132.30 · R/R 0.16 | T2 €133.93 · R/R 0.31 | T3 €135.56 · R/R 0.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €120.22


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : €-0.432 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 21 % | T3 7 %
- Kelly (position) : f* 0.313 | ¼-Kelly 0.078 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.1 | bear 60.6 | side 29.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 133.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.533% → cible +1.247% / stop −8.0%, p_fill 57%, n_eff≈21.1) : P(cible|rempli) **32%** · **EV/risk -0.031** (×p_fill ; si rempli -0.44% du capital)
  - **swing** (entrée dip −3.365% → cible +2.788% / stop −3.637%, p_fill 47%, n_eff≈17.7) : P(cible|rempli) **50%** · **EV/risk -0.055** (×p_fill ; si rempli -0.42% du capital)
  - **deep** (entrée dip −5.198% → cible +3.943% / stop −5.561%, p_fill 32%, n_eff≈15.1) : P(cible|rempli) **36%** · **EV/risk -0.030** (×p_fill ; si rempli -0.53% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→54% · +2.0%→28% · +3.0%→11% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.06% (p90 5.26%) · excursion haute méd. +1.07% / basse méd. −1.32%
- Profil de vol intra : ouverture 1.76% vs midi 0.56% vs clôture 0.781% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 17%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.83% ; recovery-V 11%
- **σ réalisé intraday** 2.243% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 77% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 128.8238 (VA 128.1538–129.6612 ; dernier close 129.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 25% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=145) : méd. 0.15% · baisse 38% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=146) : bas méd −0.5% (p90 −2.01%) · haut méd +0.3% · range méd 1.11%
- Excursion ouverture 15min (n=146) : bas méd −0.59% (p90 −2.15%) · haut méd +0.39% · range méd 1.31%
- Excursion ouverture 30min (n=146) : bas méd −0.6% (p90 −2.31%) · haut méd +0.48% · range méd 1.42%
- Excursion ouverture 60min (n=146) : bas méd −0.82% (p90 −2.71%) · haut méd +0.59% · range méd 1.57%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 73% (104/145) · gap 23% · délai 0.5min · rebond 44% (50/104) (MFE +0.84%)
   - −1.0% : fill 30min 39% · séance 64% (87/145) · gap 10% · délai 9.5min · rebond 46% (41/87) (MFE +0.93%)
   - −1.5% : fill 30min 24% · séance 51% (65/145) · gap 3% · délai 45.7min · rebond 48% (31/65) (MFE +0.76%)
   - −2.0% : fill 30min 16% · séance 36% (49/145) · gap 2% · délai 56.4min · rebond 49% (26/49) (MFE +0.99%)
   - −3.0% : fill 30min 4% · séance 25% (31/145) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 9% (11/145) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/145) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −1.11%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.08% (p90 −0.87%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=306 jambes) : jambe baissière méd −1.09% (p90 −2.5%) · ~6.0 jambes/séance
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
   - **gap-up** (66 séances) :
      · −1.0% : fill 48% (27/66) · rebond 46% (13/27)
      · −2.0% : fill 27% (12/66) · rebond 53% (7/12)
      · −3.0% : fill 17% (7/66) · rebond 82% (6/7)
      · −4.0% : fill 4% (2/66) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/66) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 42% en base · 65% si les 15 1res min sont vertes (78 cas) · 17% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=146) : COUDE à **28min** → P(séance verte=clôture>ouverture) 78% si début vert vs 16% si rouge (base 42% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 306min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -0.97% (q20 -1.94%) → **SL/trailing à −1.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.03% / q75 +1.71% → **scale +1.03% / runner +1.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **16%** (continue à baisser 58%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.23%** (au-delà de la MAE q10 -3.23%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-2.06% .. +2.22%] · haut q95 +2.45% · bas q05 -2.81%
   - 60min (n=146) : retour [-2.91% .. +2.14%] · haut q95 +2.74% · bas q05 -3.25%
   - 2h (n=146) : retour [-3.65% .. +2.15%] · haut q95 +2.92% · bas q05 -3.84%
   - 4h (n=146) : retour [-3.42% .. +2.37%] · haut q95 +2.94% · bas q05 -4.05%
   - 6h (n=146) : retour [-3.84% .. +3.28%] · haut q95 +3.7% · bas q05 -4.22%
   - session (n=146) : retour [-3.61% .. +2.85%] · haut q95 +4.0% · bas q05 -4.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.0  _(momentum baissier)_
- **ADX** : 34.6  _(tendance etablie)_
- **MACD** : hist 0.386  _(bullish_recent)_
- **BB** : %B 0.51 · largeur 8.6%
- **ATR** : 4.66 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.032  _(neutre)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 60.0  _(transition)_
- **MA** : MA20 132.58 · MA50 143.7 · MA200 131.68  _(prix > MA20)_
- **Dist MA** : MA20 +0.1% · MA50 -7.7% · MA200 +0.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92313 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
