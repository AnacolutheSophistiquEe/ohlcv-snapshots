# SRT3

**Generated** : 2026-07-21T21:37:01.621205+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €217.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €217.20 (+5.1% vs entrée) · entrée €206.74 · stop €201.57 · T1 €210.64 · R/R 0.75  
> ↳ P(T1 av. stop) 49 % · EV/risk 0.095 · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €205.96–€207.52 (mid €206.74)
- Spot actuel : €217.20 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : €201.57 (stop swing_plan-based (-12.49%))
- Targets : T1 €210.64 · R/R 0.75 | T2 €214.55 · R/R 1.51 | T3 €218.46 · R/R 2.27
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €201.57


## Edge, scénarios & sizing

- EV/risk : 0.095 | EV/share : €0.491 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 16 % | T3 10 %
- Kelly (position) : f* 0.097 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.8 | bear 16.8 | side 71.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→48% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.63% (p90 6.59%) · excursion haute méd. +1.94% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.01% vs midi 0.817% vs clôture 0.98% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 50% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr -0.013)_ ; drift intra méd. 0.337% ; recovery-V 31%
- **σ réalisé intraday** 2.4% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 56% / whipsaw 33%
- POC intraday (dernière séance, temps-au-prix) : 243.525 (VA 242.275–245.775 ; dernier close 237.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 58% · rebond 69% · **stop −2.38%** sous le fill (sous le bruit) · cible +1.65% · R/R 0.69 (high win-rate)
- Gaps overnight (n=159) : méd. -0.15% · baisse 56% (gap-down >1% 18% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.35% (p90 −1.55%) · haut méd +0.48% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.52% (p90 −1.77%) · haut méd +0.65% · range méd 1.48%
- Excursion ouverture 30min (n=160) : bas méd −0.57% (p90 −1.94%) · haut méd +0.77% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.21%) · haut méd +0.82% · range méd 1.86%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 237.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 78% (125/159) · gap 33% · délai 0.2min · rebond 52% (60/125) (MFE +1.11%)
   - −1.0% : fill 30min 45% · séance 65% (105/159) · gap 18% · délai 0.3min · rebond 61% (62/105) (MFE +1.28%)
   - −1.5% : fill 30min 35% · séance 58% (92/159) · gap 9% · délai 5.3min · rebond 69% (58/92) (MFE +1.65%)
   - −2.0% : fill 30min 22% · séance 42% (71/159) · gap 5% · délai 30.1min · rebond 57% (43/71) (MFE +1.32%)
   - −3.0% : fill 30min 5% · séance 21% (41/159) · gap 2% · délai 186.9min · rebond 49% (24/41) (MFE +1.0%)
   - −4.0% : fill 30min 3% · séance 10% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 6% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.74%) → stop au-delà de −1.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.77%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.25% (p90 −1.79%) → stop au-delà de −1.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=406 jambes) : jambe baissière méd −1.03% (p90 −2.36%) · ~6.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 86% (66/78) · rebond 72% (44/66)
      · −2.0% : fill 57% (44/78) · rebond 65% (29/44)
      · −3.0% : fill 34% (30/78) · rebond 49% (17/30)
      · −4.0% : fill 16% (16/78) · rebond 71% (12/16)
      · −5.0% : fill 8% (7/78) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 57% (19/34) · rebond 34% (8/19)
      · −2.0% : fill 44% (14/34) · rebond 37% (6/14)
      · −3.0% : fill 17% (6/34) · rebond 49% (4/6)
      · −4.0% : fill 10% (3/34) · rebond 44% (2/3)
      · −5.0% : fill 10% (3/34) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 41% (20/47) · rebond 52% (10/20)
      · −2.0% : fill 21% (13/47) · rebond 55% (8/13)
      · −3.0% : fill 5% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 1% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 60% si les 15 1res min sont vertes (90 cas) · 42% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:16** → P(séance verte=clôture>ouverture) 67% si début vert vs 35% si rouge (base 52% · écart 33 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **67%** · continue >prix actuel 44% ; creux résiduel méd -1.27% (q20 -2.35%) → **SL/trailing à −2.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.5% → **scale +1.13% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **35%** (continue à baisser 55%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.44%** (au-delà de la MAE q10 -3.44%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.01% .. +2.14%] · haut q95 +2.68% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.32% .. +2.33%] · haut q95 +2.86% · bas q05 -2.82%
   - 2h (n=160) : retour [-2.22% .. +2.71%] · haut q95 +3.12% · bas q05 -3.06%
   - 4h (n=160) : retour [-2.56% .. +2.82%] · haut q95 +3.39% · bas q05 -3.37%
   - 6h (n=160) : retour [-2.67% .. +3.56%] · haut q95 +4.26% · bas q05 -3.55%
   - session (n=160) : retour [-3.67% .. +4.91%] · haut q95 +6.25% · bas q05 -4.09%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.9  _(momentum baissier)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist -0.704  _(bearish_recent)_
- **BB** : %B 0.11 · largeur 17.7%
- **ATR** : 10.71 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.029  _(neutre)_
- **Vol ratio** : 3.68  _(volume au-dessus de la moyenne)_
- **Choppiness** : 47.1  _(transition)_
- **MA** : MA20 233.19 · MA50 230.96 · MA200 231.68  _(prix < MA20)_
- **Dist MA** : MA20 -6.9% · MA50 -6.0% · MA200 -6.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88575 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
