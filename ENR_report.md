# ENR

**Generated** : 2026-07-09T00:05:55.460685+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €152.66  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €152.66 (+0.6% vs entrée) · entrée €151.69 · stop €148.15 · T1 €158.78 · R/R 2.0  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.134 _(réel 5 s)_ (GBM 0.147) · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €150.73–€152.66 (mid €151.69)
- Spot actuel : €152.66 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €148.15 (stop swing_plan-based (-2.95%))
- Targets : T1 €158.78 · R/R 2.0 | T2 €165.87 · R/R 4.01 | T3 €172.96 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €148.15


## Edge, scénarios & sizing

- EV/risk : 0.147 | EV/share : €0.523 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 13 % | T3 4 %
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 42.6 | bear 46.7 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.359% → cible +2.09% / stop −8.0%, p_fill 87%, n_eff≈35.2) : P(cible|rempli) **28%** · **EV/risk -0.082** (×p_fill ; si rempli -0.75% du capital)
  - **swing** (entrée dip −0.628% → cible +4.674% / stop −2.337%, p_fill 83%, n_eff≈33.7) : P(cible|rempli) **29%** · **EV/risk -0.134** (×p_fill ; si rempli -0.38% du capital)
  - **deep** (entrée dip −0.916% → cible +6.609% / stop −3.305%, p_fill 87%, n_eff≈34.5) : P(cible|rempli) **29%** · **EV/risk -0.162** (×p_fill ; si rempli -0.61% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→48% · +3.0%→25% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.36% (p90 6.09%) · excursion haute méd. +1.53% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.178% vs midi 0.977% vs clôture 1.193% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.398% ; recovery-V 25%
- **σ réalisé intraday** 2.616% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 62% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 158.8487 (VA 157.4597–160.9323 ; dernier close 153.78)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 17% · rebond 67% · **stop −2.92%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.36% · baisse 40% (gap-down >1% 22% · >2% 13%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.21%) · haut méd +0.44% · range méd 1.25%
- Excursion ouverture 15min (n=160) : bas méd −0.78% (p90 −2.24%) · haut méd +0.59% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.54%) · haut méd +0.6% · range méd 1.87%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.59%) · haut méd +0.71% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 153.78 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 73% (114/159) · gap 28% · délai 0.4min · rebond 52% (58/114) (MFE +1.11%)
   - −1.0% : fill 30min 51% · séance 67% (102/159) · gap 22% · délai 1.2min · rebond 56% (59/102) (MFE +1.31%)
   - −1.5% : fill 30min 41% · séance 62% (89/159) · gap 19% · délai 10.5min · rebond 62% (56/89) (MFE +1.53%)
   - −2.0% : fill 30min 26% · séance 46% (65/159) · gap 13% · délai 6.2min · rebond 61% (39/65) (MFE +1.38%)
   - −3.0% : fill 30min 17% · séance 34% (48/159) · gap 6% · délai 25.5min · rebond 67% (35/48) (MFE +1.5%)
   - −4.0% : fill 30min 9% · séance 26% (37/159) · gap 4% · délai 285.2min · rebond 60% (25/37) (MFE +1.23%)
   - −5.0% : fill 30min 4% · séance 17% (21/159) · gap 1% · délai 203.6min · rebond 67% (14/21) (MFE +1.36%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.9%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.21%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.52%) → stop au-delà de −0.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=485 jambes) : jambe baissière méd −1.04% (p90 −2.53%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 96% (45/46) · rebond 54% (25/45)
      · −2.0% : fill 73% (33/46) · rebond 62% (22/33)
      · −3.0% : fill 62% (28/46) · rebond 61% (20/28)
      · −4.0% : fill 52% (23/46) · rebond 55% (16/23)
      · −5.0% : fill 38% (15/46) · rebond 63% (10/15)
   - **flat** (28 séances) :
      · −1.0% : fill 71% (20/28) · rebond 69% (14/20)
      · −2.0% : fill 35% (9/28) · rebond 56% (4/9)
      · −3.0% : fill 18% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 15% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 9% (2/28) · rebond 74% (1/2)
   - **gap-up** (85 séances) :
      · −1.0% : fill 48% (37/85) · rebond 52% (20/37)
      · −2.0% : fill 32% (23/85) · rebond 60% (13/23)
      · −3.0% : fill 21% (15/85) · rebond 73% (12/15)
      · −4.0% : fill 13% (10/85) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/85) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 86% si les 15 1res min sont vertes (77 cas) · 24% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 24% si rouge (base 50% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **86%** · continue >prix actuel 73% ; creux résiduel méd -1.09% (q20 -2.24%) → **SL/trailing à −2.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.3% → **scale +2.05% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **24%** (continue à baisser 63%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.08%** (au-delà de la MAE q10 -5.08%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.28% .. +2.03%] · haut q95 +2.69% · bas q05 -2.97%
   - 60min (n=160) : retour [-2.33% .. +2.13%] · haut q95 +2.76% · bas q05 -3.24%
   - 2h (n=160) : retour [-2.87% .. +2.44%] · haut q95 +3.19% · bas q05 -3.67%
   - 4h (n=160) : retour [-2.89% .. +2.65%] · haut q95 +4.11% · bas q05 -3.82%
   - 6h (n=160) : retour [-3.16% .. +3.77%] · haut q95 +4.72% · bas q05 -4.43%
   - session (n=160) : retour [-5.27% .. +4.39%] · haut q95 +5.57% · bas q05 -5.94%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.6  _(momentum baissier)_
- **ADX** : 14.4  _(pas de tendance nette)_
- **MACD** : hist -0.212  _(bearish_recent)_
- **BB** : %B 0.19 · largeur 16.8%
- **ATR** : 7.65 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.05  _(neutre)_
- **Vol ratio** : 0.46  _(volume atone)_
- **Choppiness** : 59.3  _(transition)_
- **MA** : MA20 161.02 · MA50 166.41 · MA200 140.56  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -8.3% · MA200 +8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89635 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
