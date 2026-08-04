# 207940

**Generated** : 2026-08-04T00:19:10.750731+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩1423000.00  

> 🟡 **WAIT-FOR-DIP** — spot +6.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1423000.00 (+6.2% vs entrée) · entrée ₩1340225.00 · stop ₩1259439.29 · T1 ₩1399338.59 · R/R 0.73  
> ↳ P(T1 av. stop) 71 % · EV/risk 0.238 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 122 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1328402.28–₩1352047.72 (mid ₩1340225.00)
- Spot actuel : ₩1423000.00 (+6.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1259439.29 (stop swing_plan-based (-11.49%))
- Targets : T1 ₩1399338.59 · R/R 0.73 | T2 ₩1458452.18 · R/R 1.46 | T3 ₩1517565.77 · R/R 2.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1259439.29


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : ₩-5541.070 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 15 % | T3 3 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 38.6 | bear 16.2 | side 45.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.641% → cible +1.973% / stop −8.0%, p_fill 40%, n_eff≈16.5) : P(cible|rempli) **25%** · **EV/risk +0.017** (×p_fill ; si rempli +0.34% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→52% · +2.0%→36% · +3.0%→22% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.05% (p90 6.65%) · excursion haute méd. +1.06% / basse méd. −1.87%
- Profil de vol intra : ouverture 2.488% vs midi 0.72% vs clôture 0.831% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 11% · trend ↑2%/↓3% ; spike-down 59% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.108% ; recovery-V 36%
- **σ réalisé intraday** 3.454% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 1480687.5 (VA 1470812.5–1482662.5 ; dernier close 1481000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 70% · **stop −2.98%** sous le fill (sous le bruit) · cible +1.48% · R/R 0.5 (high win-rate)
- Gaps overnight (n=144) : méd. 0.4% · baisse 34% (gap-down >1% 8% · >2% 4%)
- Excursion ouverture 5min (n=145) : bas méd −0.87% (p90 −2.6%) · haut méd +0.5% · range méd 1.62%
- Excursion ouverture 15min (n=145) : bas méd −1.07% (p90 −3.03%) · haut méd +0.64% · range méd 2.07%
- Excursion ouverture 30min (n=145) : bas méd −1.22% (p90 −3.31%) · haut méd +0.71% · range méd 2.56%
- Excursion ouverture 60min (n=145) : bas méd −1.3% (p90 −3.51%) · haut méd +0.85% · range méd 2.8%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1481000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 76% (98/144) · gap 19% · délai 1.1min · rebond 54% (44/98) (MFE +1.07%)
   - −1.0% : fill 30min 48% · séance 63% (79/144) · gap 8% · délai 2.5min · rebond 58% (36/79) (MFE +1.29%)
   - −1.5% : fill 30min 41% · séance 53% (62/144) · gap 5% · délai 3.5min · rebond 58% (30/62) (MFE +1.6%)
   - −2.0% : fill 30min 30% · séance 44% (53/144) · gap 4% · délai 6.1min · rebond 70% (30/53) (MFE +1.48%)
   - −3.0% : fill 30min 11% · séance 28% (33/144) · gap 2% · délai 83.8min · rebond 66% (19/33) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 15% (17/144) · gap 2% · délai 90.8min · rebond 64% (10/17) (MFE +1.37%)
   - −5.0% : fill 30min 2% · séance 9% (10/144) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.4%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.1%) → stop au-delà de −1.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.33%) → stop au-delà de −2.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=368 jambes) : jambe baissière méd −1.14% (p90 −2.78%) · ~8.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (34 séances) :
      · −1.0% : fill 98% (33/34) · rebond 74% (18/33)
      · −2.0% : fill 82% (28/34) · rebond 74% (15/28)
      · −3.0% : fill 39% (14/34) · rebond 64% (8/14)
      · −4.0% : fill 26% (8/34) · rebond 70% (4/8)
      · −5.0% : fill 15% (5/34) · rebond 100% (5/5)
   - **flat** (42 séances) :
      · −1.0% : fill 64% (23/42) · rebond 31% (7/23)
      · −2.0% : fill 36% (10/42) · rebond 57% (5/10)
      · −3.0% : fill 28% (7/42) · rebond 97% (6/7)
      · −4.0% : fill 16% (4/42) · rebond 100% (4/4)
      · −5.0% : fill 7% (2/42) · rebond 89% (1/2)
   - **gap-up** (68 séances) :
      · −1.0% : fill 46% (23/68) · rebond 58% (11/23)
      · −2.0% : fill 27% (15/68) · rebond 72% (10/15)
      · −3.0% : fill 23% (12/68) · rebond 49% (5/12)
      · −4.0% : fill 10% (5/68) · rebond 33% (2/5)
      · −5.0% : fill 7% (3/68) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 41% en base · 66% si les 15 1res min sont vertes (50 cas) · 26% si rouges (95 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=145) : COUDE à **33min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 41% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=52) : tient le vert **73%** · continue >prix actuel 39% ; creux résiduel méd -1.41% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.15% / q75 +2.29% → **scale +1.15% / runner +2.29%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **22%** (continue à baisser 52%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.47%** (au-delà de la MAE q10 -3.47%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-3.09% .. +3.5%] · haut q95 +3.98% · bas q05 -3.6%
   - 60min (n=145) : retour [-3.55% .. +2.94%] · haut q95 +4.39% · bas q05 -4.22%
   - 2h (n=145) : retour [-4.29% .. +3.52%] · haut q95 +4.99% · bas q05 -4.75%
   - 4h (n=145) : retour [-5.18% .. +4.25%] · haut q95 +5.13% · bas q05 -5.85%
   - 6h (n=145) : retour [-5.01% .. +4.19%] · haut q95 +5.64% · bas q05 -6.11%
   - session (n=145) : retour [-4.82% .. +3.89%] · haut q95 +5.64% · bas q05 -6.11%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.06%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 52.0  _(neutre)_
- **ADX** : 12.5  _(pas de tendance nette)_
- **MACD** : hist 5141.601  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 19.2%
- **ATR** : 80785.71 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.081  _(accumulation)_
- **Vol ratio** : 0.7  _(volume normal)_
- **Choppiness** : 59.4  _(transition)_
- **MA** : MA20 1423700.0 · MA50 1385280.0 · MA200 1610413.08  _(prix < MA20)_
- **Dist MA** : MA20 -0.0% · MA50 +2.7% · MA200 -11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80919 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
