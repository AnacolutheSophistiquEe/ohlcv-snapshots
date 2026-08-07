# 207940

**Generated** : 2026-08-07T21:55:49.759744+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1556000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1556000.00 (+4.8% vs entrée) · entrée ₩1485125.00 · stop ₩1366315.00 · T1 ₩1513366.02 · R/R 0.24  
> ↳ P(T1 av. stop) 38 % · EV/risk -0.063 · ¼-Kelly 0.059 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -1609 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1479476.80–₩1490773.20 (mid ₩1485125.00)
- Spot actuel : ₩1556000.00 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : ₩1366315.00 (stop swing_plan-based (-15.07%))
- Targets : T1 ₩1513366.02 · R/R 0.24 | T2 ₩1541607.04 · R/R 0.48 | T3 ₩1569848.06 · R/R 0.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1366315.00


## Edge, scénarios & sizing

- EV/risk : -0.063 | EV/share : ₩-7444.325 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 11 % | T3 6 %
- Kelly (position) : f* 0.238 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.0 | bear 6.3 | side 73.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→52% · +2.0%→38% · +3.0%→24% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.07% (p90 6.65%) · excursion haute méd. +1.06% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.552% vs midi 0.742% vs clôture 0.84% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 11% · trend ↑2%/↓3% ; spike-down 58% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.079% ; recovery-V 36%
- **σ réalisé intraday** 3.275% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 52% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 1502437.5 (VA 1490412.5–1511687.5 ; dernier close 1499000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 68% · **stop −2.28%** sous le fill (sous le bruit) · cible +1.74% · R/R 0.76 (high win-rate)
- Gaps overnight (n=148) : méd. 0.4% · baisse 33% (gap-down >1% 7% · >2% 3%)
- Excursion ouverture 5min (n=149) : bas méd −0.87% (p90 −2.58%) · haut méd +0.5% · range méd 1.53%
- Excursion ouverture 15min (n=149) : bas méd −1.09% (p90 −2.98%) · haut méd +0.6% · range méd 2.12%
- Excursion ouverture 30min (n=149) : bas méd −1.26% (p90 −3.38%) · haut méd +0.71% · range méd 2.48%
- Excursion ouverture 60min (n=149) : bas méd −1.3% (p90 −3.58%) · haut méd +0.85% · range méd 2.77%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1499000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 76% (101/148) · gap 19% · délai 1.2min · rebond 55% (46/101) (MFE +1.12%)
   - −1.0% : fill 30min 46% · séance 61% (80/148) · gap 7% · délai 1.9min · rebond 56% (36/80) (MFE +1.28%)
   - −1.5% : fill 30min 40% · séance 51% (63/148) · gap 4% · délai 3.3min · rebond 56% (30/63) (MFE +1.51%)
   - −2.0% : fill 30min 29% · séance 42% (54/148) · gap 3% · délai 6.3min · rebond 67% (30/54) (MFE +1.42%)
   - −3.0% : fill 30min 12% · séance 28% (34/148) · gap 2% · délai 62.4min · rebond 62% (19/34) (MFE +1.4%)
   - −4.0% : fill 30min 4% · séance 16% (18/148) · gap 2% · délai 73.5min · rebond 68% (11/18) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 8% (10/148) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.36%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.08%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −2.23%) → stop au-delà de −1.88% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=380 jambes) : jambe baissière méd −1.12% (p90 −2.77%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (35 séances) :
      · −1.0% : fill 98% (34/35) · rebond 69% (18/34)
      · −2.0% : fill 84% (29/35) · rebond 68% (15/29)
      · −3.0% : fill 43% (15/35) · rebond 54% (8/15)
      · −4.0% : fill 31% (9/35) · rebond 76% (5/9)
      · −5.0% : fill 14% (5/35) · rebond 100% (5/5)
   - **flat** (42 séances) :
      · −1.0% : fill 64% (23/42) · rebond 31% (7/23)
      · −2.0% : fill 36% (10/42) · rebond 57% (5/10)
      · −3.0% : fill 28% (7/42) · rebond 97% (6/7)
      · −4.0% : fill 16% (4/42) · rebond 100% (4/4)
      · −5.0% : fill 7% (2/42) · rebond 89% (1/2)
   - **gap-up** (71 séances) :
      · −1.0% : fill 41% (23/71) · rebond 58% (11/23)
      · −2.0% : fill 24% (15/71) · rebond 72% (10/15)
      · −3.0% : fill 20% (12/71) · rebond 49% (5/12)
      · −4.0% : fill 9% (5/71) · rebond 33% (2/5)
      · −5.0% : fill 6% (3/71) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 41% en base · 68% si les 15 1res min sont vertes (51 cas) · 26% si rouges (98 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=149) : COUDE à **33min** → P(séance verte=clôture>ouverture) 75% si début vert vs 21% si rouge (base 41% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=54) : tient le vert **75%** · continue >prix actuel 40% ; creux résiduel méd -1.26% (q20 -2.64%) → **SL/trailing à −2.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +2.52% → **scale +1.33% / runner +2.52%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **21%** (continue à baisser 52%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.45%** (au-delà de la MAE q10 -3.45%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-3.24% .. +3.45%] · haut q95 +3.84% · bas q05 -3.6%
   - 60min (n=149) : retour [-3.54% .. +2.82%] · haut q95 +4.25% · bas q05 -4.19%
   - 2h (n=149) : retour [-4.18% .. +3.46%] · haut q95 +4.77% · bas q05 -4.73%
   - 4h (n=149) : retour [-5.07% .. +4.01%] · haut q95 +5.11% · bas q05 -5.83%
   - 6h (n=149) : retour [-4.93% .. +4.12%] · haut q95 +5.43% · bas q05 -6.11%
   - session (n=149) : retour [-4.75% .. +3.76%] · haut q95 +5.43% · bas q05 -6.11%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 67.4  _(momentum haussier)_
- **ADX** : 12.0  _(pas de tendance nette)_
- **MACD** : hist 6733.844  _(pas de croisement recent)_
- **BB** : %B 0.88 · largeur 19.5%
- **ATR** : 78500.0 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.185  _(accumulation)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 59.4  _(transition)_
- **MA** : MA20 1449800.0 · MA50 1393640.0 · MA200 1608402.08  _(prix > MA20)_
- **Dist MA** : MA20 +7.3% · MA50 +11.7% · MA200 -3.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80660 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
