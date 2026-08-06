# 267260

**Generated** : 2026-08-06T21:51:50.216657+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩763000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩763000.00 (+0.8% vs entrée) · entrée ₩757000.26 · stop ₩696440.24 · T1 ₩838415.28 · R/R 1.34  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.142 _(réel 5 s)_ (GBM -0.173) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩751000.52–₩763000.00 (mid ₩757000.26)
- Spot actuel : ₩763000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩696440.24 (stop swing_plan-based (-11.32%))
- Targets : T1 ₩838415.28 · R/R 1.34 | T2 ₩845634.85 · R/R 1.46 | T3 ₩852854.42 · R/R 1.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩696440.24


## Edge, scénarios & sizing

- EV/risk : -0.173 | EV/share : ₩-10469.314 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.019 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.3 | bear 78.5 | side 15.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.783% → cible +10.755% / stop −8.0%, p_fill 98%, n_eff≈39.5) : P(cible|rempli) **1%** · **EV/risk -0.142** (×p_fill ; si rempli -1.16% du capital)
  - **swing** (entrée dip −1.733% → cible +9.438% / stop −9.756%, p_fill 93%, n_eff≈37.3) : P(cible|rempli) **27%** · **EV/risk -0.323** (×p_fill ; si rempli -3.39% du capital)
  - **deep** (entrée dip −2.551% → cible +13.347% / stop −14.756%, p_fill 91%, n_eff≈36.5) : P(cible|rempli) **29%** · **EV/risk -0.337** (×p_fill ; si rempli -5.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→48% · +3.0%→36% · +5.0%→12% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.58%) · excursion haute méd. +1.85% / basse méd. −3.81%
- Profil de vol intra : ouverture 4.386% vs midi 1.202% vs clôture 1.232% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; mean-reverting — autocorr -0.062)_ ; drift intra méd. -1.739% ; recovery-V 27%
- **σ réalisé intraday** 4.965% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 68% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 763487.5 (VA 762412.5–771012.5 ; dernier close 776000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 82% · **stop −5.38%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.38 (high win-rate)
- Gaps overnight (n=147) : méd. 1.13% · baisse 39% (gap-down >1% 21% · >2% 10%)
- Excursion ouverture 5min (n=148) : bas méd −1.74% (p90 −4.24%) · haut méd +1.03% · range méd 2.88%
- Excursion ouverture 15min (n=148) : bas méd −1.98% (p90 −4.79%) · haut méd +1.08% · range méd 3.61%
- Excursion ouverture 30min (n=148) : bas méd −2.34% (p90 −5.15%) · haut méd +1.28% · range méd 3.96%
- Excursion ouverture 60min (n=148) : bas méd −2.95% (p90 −5.72%) · haut méd +1.41% · range méd 4.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 776000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 70% (103/147) · gap 30% · délai 0.0min · rebond 53% (57/103) (MFE +1.16%)
   - −1.0% : fill 30min 54% · séance 67% (96/147) · gap 21% · délai 0.2min · rebond 57% (57/96) (MFE +1.3%)
   - −1.5% : fill 30min 47% · séance 61% (83/147) · gap 14% · délai 0.4min · rebond 66% (54/83) (MFE +1.28%)
   - −2.0% : fill 30min 43% · séance 57% (75/147) · gap 10% · délai 0.7min · rebond 69% (51/75) (MFE +1.61%)
   - −3.0% : fill 30min 34% · séance 49% (60/147) · gap 7% · délai 1.8min · rebond 78% (42/60) (MFE +1.98%)
   - −4.0% : fill 30min 24% · séance 40% (49/147) · gap 4% · délai 8.1min · rebond 74% (38/49) (MFE +2.29%)
   - −5.0% : fill 30min 16% · séance 34% (39/147) · gap 2% · délai 37.6min · rebond 82% (30/39) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.83% (p90 −3.66%) → stop au-delà de −2.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.96% (p90 −3.79%) → stop au-delà de −2.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.62% (p90 −5.19%) → stop au-delà de −3.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=757 jambes) : jambe baissière méd −1.29% (p90 −3.59%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 98% (50/51) · rebond 52% (27/50)
      · −2.0% : fill 93% (43/51) · rebond 64% (26/43)
      · −3.0% : fill 84% (37/51) · rebond 76% (25/37)
      · −4.0% : fill 71% (32/51) · rebond 73% (25/32)
      · −5.0% : fill 63% (25/51) · rebond 80% (19/25)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (79 séances) :
      · −1.0% : fill 44% (32/79) · rebond 69% (23/32)
      · −2.0% : fill 31% (20/79) · rebond 74% (16/20)
      · −3.0% : fill 22% (12/79) · rebond 77% (9/12)
      · −4.0% : fill 18% (10/79) · rebond 82% (8/10)
      · −5.0% : fill 13% (7/79) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 35% en base · 53% si les 15 1res min sont vertes (67 cas) · 25% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=148) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 69% si début vert vs 12% si rouge (base 35% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **69%** · continue >prix actuel 42% ; creux résiduel méd -1.83% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.69% → **scale +1.38% / runner +2.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **12%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.62%** (au-delà de la MAE q10 -5.62%), cible rebond +1.5% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-5.5% .. +2.69%] · haut q95 +4.23% · bas q05 -5.79%
   - 60min (n=148) : retour [-5.7% .. +2.9%] · haut q95 +4.45% · bas q05 -6.57%
   - 2h (n=148) : retour [-7.04% .. +3.69%] · haut q95 +5.17% · bas q05 -7.81%
   - 4h (n=148) : retour [-6.95% .. +3.91%] · haut q95 +5.41% · bas q05 -8.75%
   - 6h (n=148) : retour [-8.25% .. +4.41%] · haut q95 +6.67% · bas q05 -9.42%
   - session (n=148) : retour [-7.65% .. +4.34%] · haut q95 +6.76% · bas q05 -9.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.5%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.5  _(neutre)_
- **ADX** : 27.3  _(tendance etablie)_
- **MACD** : hist 10335.923  _(bullish_recent)_
- **BB** : %B 0.52 · largeur 41.3%
- **ATR** : 73142.86 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.029  _(neutre)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 42.7  _(transition)_
- **MA** : MA20 757700.0 · MA50 903360.0 · MA200 923742.72  _(prix > MA20)_
- **Dist MA** : MA20 +0.7% · MA50 -15.5% · MA200 -17.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82492 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
