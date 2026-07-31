# NEX

**Generated** : 2026-07-31T21:42:56.851295+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €131.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €131.80 (+1.4% vs entrée) · entrée €130.00 · stop €119.60 · T1 €131.52 · R/R 0.15  
> ↳ P(T1 av. stop) 38 % _(réel 5 s)_ · EV/risk -0.033 _(réel 5 s)_ (GBM -0.04) · ¼-Kelly 0.082 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €129.69–€130.30 (mid €130.00)
- Spot actuel : €131.80 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : €119.60 (stop swing_plan-based (-4.28%))
- Targets : T1 €131.52 · R/R 0.15 | T2 €133.05 · R/R 0.29 | T3 €134.58 · R/R 0.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €119.60


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : €-0.419 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 22 % | T3 7 %
- Kelly (position) : f* 0.326 | ¼-Kelly 0.082 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.5 | bear 44.5 | side 46.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 132.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.37% → cible +1.175% / stop −8.0%, p_fill 57%, n_eff≈21.6) : P(cible|rempli) **38%** · **EV/risk -0.033** (×p_fill ; si rempli -0.46% du capital)
  - **swing** (entrée dip −3.006% → cible +2.627% / stop −1.314%, p_fill 41%, n_eff≈19.6) : P(cible|rempli) **43%** · **EV/risk +0.073** (×p_fill ; si rempli +0.23% du capital)
  - **deep** (entrée dip −4.649% → cible +3.715% / stop −1.858%, p_fill 43%, n_eff≈18.2) : P(cible|rempli) **10%** · **EV/risk -0.321** (×p_fill ; si rempli -1.39% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→54% · +2.0%→28% · +3.0%→11% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.0% (p90 5.26%) · excursion haute méd. +1.07% / basse méd. −1.18%
- Profil de vol intra : ouverture 1.708% vs midi 0.532% vs clôture 0.767% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 49% · recovery-V 15%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.813% ; recovery-V 5%
- **σ réalisé intraday** 2.134% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 73% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 132.3313 (VA 128.7688–133.8313 ; dernier close 129.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 50% · **stop −1.98%** sous le fill (sous le bruit) · cible +1.03% · R/R 0.52 (high win-rate)
- Gaps overnight (n=142) : méd. 0.13% · baisse 40% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=143) : bas méd −0.46% (p90 −2.11%) · haut méd +0.3% · range méd 1.01%
- Excursion ouverture 15min (n=143) : bas méd −0.59% (p90 −2.18%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=143) : bas méd −0.6% (p90 −2.29%) · haut méd +0.45% · range méd 1.41%
- Excursion ouverture 60min (n=143) : bas méd −0.78% (p90 −2.48%) · haut méd +0.58% · range méd 1.55%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 129.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 73% (102/142) · gap 24% · délai 0.4min · rebond 44% (49/102) (MFE +0.84%)
   - −1.0% : fill 30min 40% · séance 64% (85/142) · gap 10% · délai 9.5min · rebond 43% (39/85) (MFE +0.79%)
   - −1.5% : fill 30min 23% · séance 50% (63/142) · gap 3% · délai 60.9min · rebond 44% (29/63) (MFE +0.7%)
   - −2.0% : fill 30min 16% · séance 34% (47/142) · gap 2% · délai 78.4min · rebond 43% (24/47) (MFE +0.84%)
   - −3.0% : fill 30min 5% · séance 22% (29/142) · gap 1% · délai 143.6min · rebond 50% (16/29) (MFE +1.03%)
   - −4.0% : fill 30min 1% · séance 9% (11/142) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/142) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −0.95%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=295 jambes) : jambe baissière méd −1.09% (p90 −2.43%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (34 séances) :
      · −1.0% : fill 73% (23/34) · rebond 44% (12/23)
      · −2.0% : fill 39% (11/34) · rebond 42% (5/11)
      · −3.0% : fill 27% (7/34) · rebond 32% (2/7)
      · −4.0% : fill 12% (2/34) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/34) · rebond 0% (0/0)
   - **gap-up** (64 séances) :
      · −1.0% : fill 48% (26/64) · rebond 41% (12/26)
      · −2.0% : fill 25% (11/64) · rebond 44% (6/11)
      · −3.0% : fill 14% (6/64) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/64) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/64) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 43% en base · 67% si les 15 1res min sont vertes (77 cas) · 14% si rouges (66 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=143) : COUDE à **28min** → P(séance verte=clôture>ouverture) 81% si début vert vs 14% si rouge (base 43% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **81%** · continue >prix actuel 54% ; creux résiduel méd -0.96% (q20 -1.85%) → **SL/trailing à −1.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.87% → **scale +1.18% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **14%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +0.99% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-2.09% .. +1.75%] · haut q95 +2.21% · bas q05 -2.82%
   - 60min (n=143) : retour [-2.63% .. +2.05%] · haut q95 +2.35% · bas q05 -3.18%
   - 2h (n=143) : retour [-3.54% .. +2.15%] · haut q95 +2.5% · bas q05 -3.74%
   - 4h (n=143) : retour [-3.09% .. +2.39%] · haut q95 +2.88% · bas q05 -3.87%
   - 6h (n=143) : retour [-3.86% .. +3.37%] · haut q95 +3.8% · bas q05 -4.17%
   - session (n=143) : retour [-3.61% .. +2.87%] · haut q95 +4.18% · bas q05 -4.66%


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.4  _(neutre)_
- **ADX** : 34.2  _(tendance etablie)_
- **MACD** : hist 0.259  _(pas de croisement recent)_
- **BB** : %B 0.4 · largeur 10.1%
- **ATR** : 4.67 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.06  _(distribution)_
- **Vol ratio** : 1.79  _(volume au-dessus de la moyenne)_
- **Choppiness** : 56.0  _(transition)_
- **MA** : MA20 133.13 · MA50 144.34 · MA200 131.62  _(prix < MA20)_
- **Dist MA** : MA20 -1.0% · MA50 -8.7% · MA200 +0.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92471 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
