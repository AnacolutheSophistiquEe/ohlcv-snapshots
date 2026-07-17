# PRY

**Generated** : 2026-07-17T00:12:36.578817+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €130.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot €130.50 (+6.5% vs entrée) · entrée €122.50 · stop €120.47 · T1 €126.55 · R/R 2.0  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.216 · ¼-Kelly 0.016 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -172 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €121.69–€123.31 (mid €122.50)
- Spot actuel : €130.50 (+6.5% au-dessus de la zone — repli à attendre)
- Stop : €120.47 (stop swing_plan-based (-7.69%))
- Targets : T1 €126.55 · R/R 2.0 | T2 €130.61 · R/R 4.0 | T3 €134.67 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €120.47


## Edge, scénarios & sizing

- EV/risk : 0.216 | EV/share : €0.439 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 19 % | T3 4 %
- Kelly (position) : f* 0.063 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.1 | bear 30.2 | side 47.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 130.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.792% → cible +1.481% / stop −1.5%, p_fill 36%, n_eff≈14.8) : P(cible|rempli) **31%** · **EV/risk -0.064** (×p_fill ; si rempli -0.26% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→66% · +2.0%→44% · +3.0%→34% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.97% (p90 6.32%) · excursion haute méd. +1.67% / basse méd. −1.47%
- Profil de vol intra : ouverture 2.241% vs midi 0.813% vs clôture 1.11% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 50% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr 0.002)_ ; drift intra méd. -0.223% ; recovery-V 17%
- **σ réalisé intraday** 2.653% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 61% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 137.02 (VA 136.54–137.66 ; dernier close 134.34)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 33% · rebond 62% · **stop −3.15%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.51 (high win-rate)
- Gaps overnight (n=132) : méd. 0.14% · baisse 44% (gap-down >1% 20% · >2% 12%)
- Excursion ouverture 5min (n=133) : bas méd −0.61% (p90 −2.34%) · haut méd +0.38% · range méd 1.31%
- Excursion ouverture 15min (n=133) : bas méd −0.77% (p90 −2.87%) · haut méd +0.65% · range méd 1.69%
- Excursion ouverture 30min (n=133) : bas méd −0.9% (p90 −3.08%) · haut méd +0.77% · range méd 1.81%
- Excursion ouverture 60min (n=133) : bas méd −1.05% (p90 −3.08%) · haut méd +0.9% · range méd 2.07%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 134.34 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (96/132) · gap 27% · délai 0.2min · rebond 62% (61/96) (MFE +1.37%)
   - −1.0% : fill 30min 50% · séance 63% (81/132) · gap 20% · délai 0.2min · rebond 58% (49/81) (MFE +1.57%)
   - −1.5% : fill 30min 34% · séance 52% (69/132) · gap 17% · délai 0.4min · rebond 52% (38/69) (MFE +1.07%)
   - −2.0% : fill 30min 26% · séance 42% (55/132) · gap 12% · délai 3.8min · rebond 55% (34/55) (MFE +1.2%)
   - −3.0% : fill 30min 14% · séance 33% (40/132) · gap 5% · délai 79.6min · rebond 62% (27/40) (MFE +1.6%)
   - −4.0% : fill 30min 4% · séance 18% (20/132) · gap 2% · délai 193.7min · rebond 65% (14/20) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 12% (14/132) · gap 2% · délai 274.5min · rebond 81% (11/14) (MFE +1.43%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.17% (p90 −1.69%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.57%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=400 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 87% (43/48) · rebond 52% (25/43)
      · −2.0% : fill 67% (34/48) · rebond 60% (23/34)
      · −3.0% : fill 56% (26/48) · rebond 62% (19/26)
      · −4.0% : fill 30% (13/48) · rebond 63% (9/13)
      · −5.0% : fill 24% (10/48) · rebond 86% (8/10)
   - **flat** (25 séances) :
      · −1.0% : fill 60% (13/25) · rebond 59% (8/13)
      · −2.0% : fill 30% (6/25) · rebond 75% (4/6)
      · −3.0% : fill 28% (5/25) · rebond 40% (2/5)
      · −4.0% : fill 13% (3/25) · rebond 59% (2/3)
      · −5.0% : fill 7% (2/25) · rebond 25% (1/2)
   - **gap-up** (59 séances) :
      · −1.0% : fill 44% (25/59) · rebond 68% (16/25)
      · −2.0% : fill 25% (15/59) · rebond 35% (7/15)
      · −3.0% : fill 16% (9/59) · rebond 75% (6/9)
      · −4.0% : fill 10% (4/59) · rebond 73% (3/4)
      · −5.0% : fill 3% (2/59) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 53% en base · 78% si les 15 1res min sont vertes (64 cas) · 30% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=133) : COUDE à **1:04** → P(séance verte=clôture>ouverture) 86% si début vert vs 24% si rouge (base 53% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **86%** · continue >prix actuel 66% ; creux résiduel méd -1.22% (q20 -2.13%) → **SL/trailing à −2.13%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.68% / q75 +2.51% → **scale +1.68% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **24%** (continue à baisser 60%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.09%** (au-delà de la MAE q10 -4.09%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-2.92% .. +2.74%] · haut q95 +3.46% · bas q05 -3.38%
   - 60min (n=133) : retour [-2.76% .. +2.63%] · haut q95 +3.94% · bas q05 -3.44%
   - 2h (n=133) : retour [-3.44% .. +3.61%] · haut q95 +4.16% · bas q05 -3.63%
   - 4h (n=133) : retour [-3.36% .. +3.71%] · haut q95 +4.63% · bas q05 -4.28%
   - 6h (n=133) : retour [-3.67% .. +3.82%] · haut q95 +5.39% · bas q05 -4.53%
   - session (n=133) : retour [-4.62% .. +4.97%] · haut q95 +6.14% · bas q05 -5.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.3% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.5  _(momentum baissier)_
- **ADX** : 21.7  _(pas de tendance nette)_
- **MACD** : hist -1.173  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 19.9%
- **ATR** : 5.96 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.104  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 50.1  _(transition)_
- **MA** : MA20 141.77 · MA50 145.83 · MA200 108.42  _(prix < MA20)_
- **Dist MA** : MA20 -7.9% · MA50 -10.5% · MA200 +20.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92530 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
