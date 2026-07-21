# SRT3

**Generated** : 2026-07-21T00:03:09.308023+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €237.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €237.90 (+4.2% vs entrée) · entrée €228.25 · stop €224.45 · T1 €235.84 · R/R 2.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.041 · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €226.73–€229.76 (mid €228.25)
- Spot actuel : €237.90 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : €224.45 (stop swing_plan-based (-5.65%))
- Targets : T1 €235.84 · R/R 2.0 | T2 €243.43 · R/R 3.99 | T3 €251.02 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €224.45


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : €0.155 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 18 % | T3 7 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.4 | bear 6.5 | side 70.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 476.0 (= 2 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.846% → cible +1.487% / stop −2.5%, p_fill 31%, n_eff≈18.9) : P(cible|rempli) **33%** · **EV/risk -0.029** (×p_fill ; si rempli -0.23% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→49% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.61% (p90 6.59%) · excursion haute méd. +1.96% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.028% vs midi 0.829% vs clôture 0.978% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 49% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr -0.013)_ ; drift intra méd. 0.45% ; recovery-V 34%
- **σ réalisé intraday** 2.412% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 54% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 250.7394 (VA 248.6631–250.9281 ; dernier close 244.7)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 68% · **stop −2.4%** sous le fill (sous le bruit) · cible +1.58% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 55% (gap-down >1% 18% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.34% (p90 −1.55%) · haut méd +0.56% · range méd 1.22%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.82%) · haut méd +0.66% · range méd 1.54%
- Excursion ouverture 30min (n=160) : bas méd −0.54% (p90 −1.94%) · haut méd +0.8% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −2.22%) · haut méd +0.84% · range méd 1.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 244.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 78% (125/159) · gap 32% · délai 0.2min · rebond 51% (59/125) (MFE +1.07%)
   - −1.0% : fill 30min 44% · séance 64% (105/159) · gap 18% · délai 0.4min · rebond 60% (61/105) (MFE +1.21%)
   - −1.5% : fill 30min 34% · séance 57% (92/159) · gap 9% · délai 6.5min · rebond 68% (57/92) (MFE +1.58%)
   - −2.0% : fill 30min 22% · séance 41% (70/159) · gap 5% · délai 21.4min · rebond 60% (43/70) (MFE +1.49%)
   - −3.0% : fill 30min 5% · séance 19% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 3% · séance 10% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 6% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.22% (p90 −1.74%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.77%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.25% (p90 −1.79%) → stop au-delà de −1.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=409 jambes) : jambe baissière méd −1.02% (p90 −2.28%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 85% (66/78) · rebond 70% (43/66)
      · −2.0% : fill 55% (43/78) · rebond 70% (29/43)
      · −3.0% : fill 31% (29/78) · rebond 56% (17/29)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 60% si les 15 1res min sont vertes (90 cas) · 44% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:16** → P(séance verte=clôture>ouverture) 70% si début vert vs 35% si rouge (base 53% · écart 35 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **70%** · continue >prix actuel 46% ; creux résiduel méd -1.21% (q20 -2.28%) → **SL/trailing à −2.28%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.12% / q75 +2.59% → **scale +1.12% / runner +2.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **35%** (continue à baisser 55%) → **RÉDUIRE ~65%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.44%** (au-delà de la MAE q10 -3.44%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.03% .. +2.14%] · haut q95 +2.69% · bas q05 -2.62%
   - 60min (n=160) : retour [-2.33% .. +2.34%] · haut q95 +2.86% · bas q05 -2.84%
   - 2h (n=160) : retour [-2.22% .. +2.72%] · haut q95 +3.13% · bas q05 -3.1%
   - 4h (n=160) : retour [-2.56% .. +2.82%] · haut q95 +3.4% · bas q05 -3.39%
   - 6h (n=160) : retour [-2.67% .. +3.57%] · haut q95 +4.33% · bas q05 -3.6%
   - session (n=160) : retour [-3.68% .. +4.96%] · haut q95 +6.27% · bas q05 -4.14%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 56.3  _(momentum haussier)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist 1.235  _(pas de croisement recent)_
- **BB** : %B 0.61 · largeur 18.4%
- **ATR** : 8.84 (60.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.136  _(accumulation)_
- **Vol ratio** : 0.35  _(volume atone)_
- **Choppiness** : 49.4  _(transition)_
- **MA** : MA20 232.99 · MA50 230.84 · MA200 231.69  _(prix > MA20)_
- **Dist MA** : MA20 +2.1% · MA50 +3.1% · MA200 +2.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91543 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
