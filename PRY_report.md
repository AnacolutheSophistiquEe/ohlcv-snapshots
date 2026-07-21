# PRY

**Generated** : 2026-07-21T21:47:00.006818+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €130.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €130.40 (+2.8% vs entrée) · entrée €126.79 · stop €124.89 · T1 €128.69 · R/R 1.0  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.061 _(réel 5 s)_ (GBM 0.071) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €126.41–€127.17 (mid €126.79)
- Spot actuel : €130.40 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : €124.89 (stop swing_plan-based (-7.67%))
- Targets : T1 €128.69 · R/R 1.0 | T2 €130.60 · R/R 2.01 | T3 €132.50 · R/R 3.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €124.89


## Edge, scénarios & sizing

- EV/risk : 0.071 | EV/share : €0.134 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 29 % | T3 11 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.2 | bear 54.0 | side 17.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 130.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.772% → cible +1.503% / stop −1.5%, p_fill 45%, n_eff≈15.8) : P(cible|rempli) **31%** · **EV/risk -0.061** (×p_fill ; si rempli -0.20% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→68% · +2.0%→44% · +3.0%→32% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.02% (p90 6.32%) · excursion haute méd. +1.67% / basse méd. −1.49%
- Profil de vol intra : ouverture 2.279% vs midi 0.813% vs clôture 1.125% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.133 ; neutre — autocorr 0.014)_ ; drift intra méd. -0.545% ; recovery-V 14%
- **σ réalisé intraday** 2.66% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 66% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 127.6508 (VA 127.1848–128.3498 ; dernier close 124.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 35% · rebond 61% · **stop −2.89%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.55 (high win-rate)
- Gaps overnight (n=135) : méd. 0.2% · baisse 44% (gap-down >1% 21% · >2% 13%)
- Excursion ouverture 5min (n=136) : bas méd −0.68% (p90 −2.16%) · haut méd +0.45% · range méd 1.3%
- Excursion ouverture 15min (n=136) : bas méd −0.79% (p90 −2.75%) · haut méd +0.67% · range méd 1.72%
- Excursion ouverture 30min (n=136) : bas méd −0.91% (p90 −2.96%) · haut méd +0.84% · range méd 1.86%
- Excursion ouverture 60min (n=136) : bas méd −1.09% (p90 −3.21%) · haut méd +0.91% · range méd 2.1%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 124.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 71% (98/135) · gap 28% · délai 0.2min · rebond 59% (61/98) (MFE +1.16%)
   - −1.0% : fill 30min 50% · séance 63% (83/135) · gap 21% · délai 0.2min · rebond 55% (49/83) (MFE +1.46%)
   - −1.5% : fill 30min 34% · séance 53% (71/135) · gap 18% · délai 0.4min · rebond 52% (39/71) (MFE +1.07%)
   - −2.0% : fill 30min 26% · séance 43% (57/135) · gap 13% · délai 3.8min · rebond 55% (35/57) (MFE +1.2%)
   - −3.0% : fill 30min 15% · séance 35% (42/135) · gap 5% · délai 72.3min · rebond 61% (28/42) (MFE +1.6%)
   - −4.0% : fill 30min 4% · séance 20% (22/135) · gap 2% · délai 160.8min · rebond 62% (15/22) (MFE +1.31%)
   - −5.0% : fill 30min 2% · séance 13% (15/135) · gap 1% · délai 332.6min · rebond 84% (12/15) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −1.64%) → stop au-delà de −1.28% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.28% (p90 −1.6%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.24% (p90 −1.57%) → stop au-delà de −1.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.07% (p90 −2.48%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 88% (44/49) · rebond 49% (25/44)
      · −2.0% : fill 69% (35/49) · rebond 63% (24/35)
      · −3.0% : fill 59% (27/49) · rebond 66% (20/27)
      · −4.0% : fill 33% (14/49) · rebond 53% (9/14)
      · −5.0% : fill 28% (11/49) · rebond 89% (9/11)
   - **flat** (25 séances) :
      · −1.0% : fill 60% (13/25) · rebond 59% (8/13)
      · −2.0% : fill 30% (6/25) · rebond 75% (4/6)
      · −3.0% : fill 28% (5/25) · rebond 40% (2/5)
      · −4.0% : fill 13% (3/25) · rebond 59% (2/3)
      · −5.0% : fill 7% (2/25) · rebond 25% (1/2)
   - **gap-up** (61 séances) :
      · −1.0% : fill 45% (26/61) · rebond 62% (16/26)
      · −2.0% : fill 27% (16/61) · rebond 30% (7/16)
      · −3.0% : fill 19% (10/61) · rebond 59% (6/10)
      · −4.0% : fill 13% (5/61) · rebond 81% (4/5)
      · −5.0% : fill 3% (2/61) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 50% en base · 78% si les 15 1res min sont vertes (64 cas) · 26% si rouges (72 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=136) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 85% si début vert vs 23% si rouge (base 50% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **85%** · continue >prix actuel 65% ; creux résiduel méd -1.26% (q20 -2.15%) → **SL/trailing à −2.15%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.59% / q75 +2.65% → **scale +1.59% / runner +2.65%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **23%** (continue à baisser 62%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-2.89% .. +2.72%] · haut q95 +3.45% · bas q05 -3.37%
   - 60min (n=136) : retour [-2.93% .. +2.5%] · haut q95 +3.92% · bas q05 -3.49%
   - 2h (n=136) : retour [-3.6% .. +3.51%] · haut q95 +4.11% · bas q05 -3.7%
   - 4h (n=136) : retour [-3.46% .. +3.68%] · haut q95 +4.58% · bas q05 -4.48%
   - 6h (n=136) : retour [-3.72% .. +3.79%] · haut q95 +5.12% · bas q05 -4.68%
   - session (n=136) : retour [-4.34% .. +4.85%] · haut q95 +6.11% · bas q05 -5.67%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.1% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.4%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 36.6  _(momentum baissier)_
- **ADX** : 25.0  _(tendance etablie)_
- **MACD** : hist -1.237  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 20.9%
- **ATR** : 6.02 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.18  _(distribution)_
- **Vol ratio** : 1.01  _(volume normal)_
- **Choppiness** : 47.9  _(transition)_
- **MA** : MA20 138.04 · MA50 144.3 · MA200 109.05  _(prix < MA20)_
- **Dist MA** : MA20 -5.5% · MA50 -9.6% · MA200 +19.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93055 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
