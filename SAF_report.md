# SAF

**Generated** : 2026-07-17T21:41:59.070069+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €329.50  

> 🟡 **WAIT-FOR-DIP** — spot +2.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €329.50 (+2.9% vs entrée) · entrée €320.13 · stop €313.73 · T1 €323.43 · R/R 0.52  
> ↳ P(T1 av. stop) 57 % · EV/risk 0.032 · ¼-Kelly 0.019 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €319.47–€320.79 (mid €320.13)
- Spot actuel : €329.50 (+2.9% au-dessus de la zone — repli à attendre)
- Stop : €313.73 (stop swing_plan-based (-7.33%))
- Targets : T1 €323.43 · R/R 0.52 | T2 €326.73 · R/R 1.03 | T3 €330.04 · R/R 1.55
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €313.73


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : €0.207 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 35 % | T3 14 %
- Kelly (position) : f* 0.076 | ¼-Kelly 0.019 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.5 | bear 9.5 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→57% · +2.0%→38% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.72% (p90 4.55%) · excursion haute méd. +1.52% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.621% vs midi 0.629% vs clôture 0.759% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (151 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 40% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. 0.138% ; recovery-V 30%
- **σ réalisé intraday** 1.793% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 57% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 328.625 (VA 325.435–329.495 ; dernier close 328.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=150) : méd. -0.06% · baisse 52% (gap-down >1% 11% · >2% 2%)
- Excursion ouverture 5min (n=151) : bas méd −0.44% (p90 −1.5%) · haut méd +0.21% · range méd 0.92%
- Excursion ouverture 15min (n=151) : bas méd −0.53% (p90 −1.62%) · haut méd +0.38% · range méd 1.17%
- Excursion ouverture 30min (n=151) : bas méd −0.59% (p90 −1.68%) · haut méd +0.48% · range méd 1.28%
- Excursion ouverture 60min (n=151) : bas méd −0.72% (p90 −1.91%) · haut méd +0.58% · range méd 1.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 328.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 67% (106/150) · gap 28% · délai 0.2min · rebond 38% (39/106) (MFE +0.76%)
   - −1.0% : fill 30min 43% · séance 54% (78/150) · gap 11% · délai 0.4min · rebond 41% (28/78) (MFE +0.62%)
   - −1.5% : fill 30min 30% · séance 46% (67/150) · gap 4% · délai 15.9min · rebond 40% (23/67) (MFE +0.89%)
   - −2.0% : fill 30min 13% · séance 36% (49/150) · gap 2% · délai 75.5min · rebond 44% (21/49) (MFE +0.78%)
   - −3.0% : fill 30min 4% · séance 19% (28/150) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 9% (13/150) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/150) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=180 jambes) : jambe baissière méd −1.09% (p90 −2.59%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 81% (43/54) · rebond 39% (16/43)
      · −2.0% : fill 61% (31/54) · rebond 44% (14/31)
      · −3.0% : fill 32% (17/54) · rebond 50% (9/17)
      · −4.0% : fill 17% (9/54) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/54) · rebond 0% (0/2)
   - **flat** (41 séances) :
      · −1.0% : fill 44% (17/41) · rebond 68% (9/17)
      · −2.0% : fill 15% (7/41) · rebond 50% (3/7)
      · −3.0% : fill 8% (4/41) · rebond 69% (3/4)
      · −4.0% : fill 2% (1/41) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/41) · rebond 0% (0/0)
   - **gap-up** (55 séances) :
      · −1.0% : fill 30% (18/55) · rebond 17% (3/18)
      · −2.0% : fill 22% (11/55) · rebond 43% (4/11)
      · −3.0% : fill 14% (7/55) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/55) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=151) : 53% en base · 72% si les 15 1res min sont vertes (67 cas) · 34% si rouges (84 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=151) : COUDE à **44min** → P(séance verte=clôture>ouverture) 82% si début vert vs 28% si rouge (base 53% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **82%** · continue >prix actuel 64% ; creux résiduel méd -0.57% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.78% → **scale +1.32% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **28%** (continue à baisser 51%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.55%** (au-delà de la MAE q10 -2.55%), cible rebond +0.92% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=151) : retour [-1.59% .. +1.58%] · haut q95 +1.94% · bas q05 -2.23%
   - 60min (n=151) : retour [-1.65% .. +2.16%] · haut q95 +2.7% · bas q05 -2.35%
   - 2h (n=151) : retour [-2.28% .. +2.2%] · haut q95 +2.82% · bas q05 -2.95%
   - 4h (n=151) : retour [-2.25% .. +2.19%] · haut q95 +3.31% · bas q05 -3.09%
   - 6h (n=151) : retour [-2.33% .. +3.01%] · haut q95 +3.47% · bas q05 -3.41%
   - session (n=151) : retour [-3.46% .. +3.28%] · haut q95 +3.72% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.0% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.66%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 45.0  _(momentum baissier)_
- **ADX** : 21.5  _(pas de tendance nette)_
- **MACD** : hist -3.667  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 11.4%
- **ATR** : 8.79 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.285  _(accumulation)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 43.8  _(transition)_
- **MA** : MA20 338.94 · MA50 312.86 · MA200 303.52  _(prix < MA20)_
- **Dist MA** : MA20 -2.8% · MA50 +5.3% · MA200 +8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88231 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
