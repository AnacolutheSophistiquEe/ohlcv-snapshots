# SRT3

**Generated** : 2026-07-23T21:36:57.260870+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €221.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot €221.80 (+5.5% vs entrée) · entrée €210.19 · stop €203.88 · T1 €213.89 · R/R 0.59  
> ↳ P(T1 av. stop) 54 % · EV/risk 0.075 · ¼-Kelly 0.038 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €209.45–€210.93 (mid €210.19)
- Spot actuel : €221.80 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : €203.88 (stop swing_plan-based (-13.26%))
- Targets : T1 €213.89 · R/R 0.59 | T2 €217.59 · R/R 1.17 | T3 €221.29 · R/R 1.76
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €203.88


## Edge, scénarios & sizing

- EV/risk : 0.075 | EV/share : €0.471 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 22 % | T3 10 %
- Kelly (position) : f* 0.153 | ¼-Kelly 0.038 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.4 | bear 51.6 | side 36.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→48% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.65% (p90 6.82%) · excursion haute méd. +1.94% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.039% vs midi 0.858% vs clôture 1.012% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.006)_ ; drift intra méd. 0.035% ; recovery-V 34%
- **σ réalisé intraday** 2.785% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 56% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 222.9456 (VA 217.7256–227.1869 ; dernier close 225.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 59% · rebond 72% · **stop −2.49%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.69 (high win-rate)
- Gaps overnight (n=159) : méd. -0.1% · baisse 54% (gap-down >1% 18% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.39% (p90 −1.86%) · haut méd +0.48% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.54% (p90 −1.96%) · haut méd +0.61% · range méd 1.59%
- Excursion ouverture 30min (n=160) : bas méd −0.61% (p90 −2.23%) · haut méd +0.68% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.71% (p90 −2.59%) · haut méd +0.75% · range méd 1.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 225.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 79% (126/159) · gap 32% · délai 0.2min · rebond 55% (62/126) (MFE +1.17%)
   - −1.0% : fill 30min 47% · séance 66% (106/159) · gap 18% · délai 0.3min · rebond 63% (64/106) (MFE +1.37%)
   - −1.5% : fill 30min 38% · séance 59% (93/159) · gap 8% · délai 3.3min · rebond 72% (60/93) (MFE +1.72%)
   - −2.0% : fill 30min 23% · séance 43% (71/159) · gap 5% · délai 21.9min · rebond 59% (43/71) (MFE +1.51%)
   - −3.0% : fill 30min 7% · séance 22% (41/159) · gap 2% · délai 184.1min · rebond 53% (24/41) (MFE +1.5%)
   - −4.0% : fill 30min 5% · séance 11% (20/159) · gap 1% · délai 85.0min · rebond 72% (15/20) (MFE +1.56%)
   - −5.0% : fill 30min 1% · séance 8% (11/159) · gap 1% · délai 148.6min · rebond 56% (8/11) (MFE +2.14%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −1.97%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.18% (p90 −1.97%) → stop au-delà de −1.12% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −2.81%) → stop au-delà de −1.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.04% (p90 −2.52%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (77 séances) :
      · −1.0% : fill 86% (65/77) · rebond 72% (44/65)
      · −2.0% : fill 56% (43/77) · rebond 65% (28/43)
      · −3.0% : fill 33% (29/77) · rebond 49% (16/29)
      · −4.0% : fill 16% (15/77) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/77) · rebond 92% (6/7)
   - **flat** (35 séances) :
      · −1.0% : fill 60% (20/35) · rebond 43% (9/20)
      · −2.0% : fill 49% (15/35) · rebond 48% (7/15)
      · −3.0% : fill 23% (7/35) · rebond 66% (5/7)
      · −4.0% : fill 17% (4/35) · rebond 70% (3/4)
      · −5.0% : fill 17% (4/35) · rebond 24% (2/4)
   - **gap-up** (47 séances) :
      · −1.0% : fill 44% (21/47) · rebond 58% (11/21)
      · −2.0% : fill 20% (13/47) · rebond 55% (8/13)
      · −3.0% : fill 5% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 1% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 60% si les 15 1res min sont vertes (89 cas) · 43% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 63% si début vert vs 40% si rouge (base 52% · écart 24 pts) ; prédictivité sature ensuite (plafond brut 268min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=85) : tient le vert **63%** · continue >prix actuel 48% ; creux résiduel méd -1.44% (q20 -2.46%) → **SL/trailing à −2.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.36% / q75 +2.74% → **scale +1.36% / runner +2.74%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **40%** (continue à baisser 55%) → **RÉDUIRE ~61%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.08%** (au-delà de la MAE q10 -5.08%), cible rebond +1.67% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.31% .. +2.12%] · haut q95 +2.67% · bas q05 -2.91%
   - 60min (n=160) : retour [-2.3% .. +2.32%] · haut q95 +2.84% · bas q05 -3.25%
   - 2h (n=160) : retour [-2.21% .. +2.67%] · haut q95 +3.11% · bas q05 -3.76%
   - 4h (n=160) : retour [-2.81% .. +2.82%] · haut q95 +3.38% · bas q05 -3.82%
   - 6h (n=160) : retour [-2.89% .. +3.55%] · haut q95 +4.14% · bas q05 -4.58%
   - session (n=160) : retour [-3.81% .. +4.81%] · haut q95 +6.18% · bas q05 -4.97%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.2  _(neutre)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist -2.114  _(bearish_recent)_
- **BB** : %B 0.24 · largeur 18.0%
- **ATR** : 12.35 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.056  _(distribution)_
- **Vol ratio** : 2.8  _(volume au-dessus de la moyenne)_
- **Choppiness** : 52.5  _(transition)_
- **MA** : MA20 232.86 · MA50 231.32 · MA200 231.62  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -4.1% · MA200 -4.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89363 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
