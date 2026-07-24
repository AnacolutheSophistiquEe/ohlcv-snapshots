# PRY

**Generated** : 2026-07-24T00:10:28.621273+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €125.25  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €125.25 (+1.9% vs entrée) · entrée €122.92 · stop €121.08 · T1 €124.79 · R/R 1.02  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk -0.17 _(réel 5 s)_ (GBM 0.034) · ¼-Kelly 0.003 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -33 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €122.55–€123.30 (mid €122.92)
- Spot actuel : €125.25 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €121.08 (stop swing_plan-based (-5.71%))
- Targets : T1 €124.79 · R/R 1.02 | T2 €126.65 · R/R 2.03 | T3 €128.51 · R/R 3.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €121.08


## Edge, scénarios & sizing

- EV/risk : 0.034 | EV/share : €0.063 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 27 % | T3 9 %
- Kelly (position) : f* 0.014 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 26.0 | bear 55.8 | side 18.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 125.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.858% → cible +1.516% / stop −1.5%, p_fill 49%, n_eff≈18.3) : P(cible|rempli) **14%** · **EV/risk -0.170** (×p_fill ; si rempli -0.53% du capital)
  - **swing** (entrée dip −4.085% → cible +3.389% / stop −1.695%, p_fill 42%, n_eff≈14.9) : P(cible|rempli) **26%** · **EV/risk -0.104** (×p_fill ; si rempli -0.42% du capital)
  - **deep** (entrée dip −6.315% → cible +4.793% / stop −2.397%, p_fill 33%, n_eff≈12.2) : P(cible|rempli) **52%** · **EV/risk +0.173** (×p_fill ; si rempli +1.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→66% · +2.0%→42% · +3.0%→31% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.92% (p90 6.32%) · excursion haute méd. +1.52% / basse méd. −1.53%
- Profil de vol intra : ouverture 2.265% vs midi 0.801% vs clôture 1.135% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.432% ; recovery-V 12%
- **σ réalisé intraday** 2.646% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 65% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 128.9332 (VA 127.9782–129.5062 ; dernier close 128.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 61% · **stop −2.89%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.55 (high win-rate)
- Gaps overnight (n=137) : méd. 0.2% · baisse 42% (gap-down >1% 20% · >2% 13%)
- Excursion ouverture 5min (n=138) : bas méd −0.68% (p90 −2.12%) · haut méd +0.53% · range méd 1.35%
- Excursion ouverture 15min (n=138) : bas méd −0.79% (p90 −2.6%) · haut méd +0.67% · range méd 1.72%
- Excursion ouverture 30min (n=138) : bas méd −0.91% (p90 −2.95%) · haut méd +0.84% · range méd 1.86%
- Excursion ouverture 60min (n=138) : bas méd −1.09% (p90 −3.19%) · haut méd +0.91% · range méd 2.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 128.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 70% (99/137) · gap 27% · délai 0.2min · rebond 60% (62/99) (MFE +1.18%)
   - −1.0% : fill 30min 50% · séance 63% (84/137) · gap 20% · délai 0.3min · rebond 56% (50/84) (MFE +1.47%)
   - −1.5% : fill 30min 33% · séance 53% (72/137) · gap 17% · délai 0.7min · rebond 50% (39/72) (MFE +0.93%)
   - −2.0% : fill 30min 25% · séance 43% (58/137) · gap 13% · délai 4.0min · rebond 57% (36/58) (MFE +1.24%)
   - −3.0% : fill 30min 15% · séance 34% (42/137) · gap 5% · délai 72.3min · rebond 61% (28/42) (MFE +1.6%)
   - −4.0% : fill 30min 4% · séance 20% (22/137) · gap 2% · délai 160.8min · rebond 62% (15/22) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 12% (15/137) · gap 1% · délai 332.6min · rebond 84% (12/15) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.2% (p90 −1.62%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.6%) → stop au-delà de −1.05% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.09% (p90 −1.56%) → stop au-delà de −1.02% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=416 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 88% (44/49) · rebond 49% (25/44)
      · −2.0% : fill 69% (35/49) · rebond 63% (24/35)
      · −3.0% : fill 59% (27/49) · rebond 66% (20/27)
      · −4.0% : fill 33% (14/49) · rebond 53% (9/14)
      · −5.0% : fill 28% (11/49) · rebond 89% (9/11)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 43% (26/62) · rebond 62% (16/26)
      · −2.0% : fill 26% (16/62) · rebond 30% (7/16)
      · −3.0% : fill 18% (10/62) · rebond 59% (6/10)
      · −4.0% : fill 12% (5/62) · rebond 81% (4/5)
      · −5.0% : fill 3% (2/62) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 50% en base · 78% si les 15 1res min sont vertes (65 cas) · 26% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=138) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 86% si début vert vs 22% si rouge (base 50% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **86%** · continue >prix actuel 66% ; creux résiduel méd -1.24% (q20 -2.11%) → **SL/trailing à −2.11%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +2.65% → **scale +1.65% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **22%** (continue à baisser 60%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.17% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-2.87% .. +2.71%] · haut q95 +3.45% · bas q05 -3.36%
   - 60min (n=138) : retour [-2.92% .. +2.42%] · haut q95 +3.92% · bas q05 -3.48%
   - 2h (n=138) : retour [-3.59% .. +3.43%] · haut q95 +4.11% · bas q05 -3.69%
   - 4h (n=138) : retour [-3.46% .. +3.66%] · haut q95 +4.55% · bas q05 -4.47%
   - 6h (n=138) : retour [-3.71% .. +3.76%] · haut q95 +4.97% · bas q05 -4.65%
   - session (n=138) : retour [-4.34% .. +4.79%] · haut q95 +6.06% · bas q05 -5.58%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.1% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.8  _(survente)_
- **ADX** : 26.8  _(tendance etablie)_
- **MACD** : hist -1.04  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 20.9%
- **ATR** : 5.78 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.189  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 50.0  _(transition)_
- **MA** : MA20 135.91 · MA50 143.15 · MA200 109.45  _(prix < MA20)_
- **Dist MA** : MA20 -7.8% · MA50 -12.5% · MA200 +14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93563 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
