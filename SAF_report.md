# SAF

**Generated** : 2026-07-23T21:40:47.161940+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €321.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot €321.40 (+2.3% vs entrée) · entrée €314.06 · stop €307.78 · T1 €317.24 · R/R 0.51  
> ↳ P(T1 av. stop) 55 % · EV/risk 0.016 · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €313.42–€314.70 (mid €314.06)
- Spot actuel : €321.40 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : €307.78 (stop swing_plan-based (-6.1%))
- Targets : T1 €317.24 · R/R 0.51 | T2 €320.43 · R/R 1.01 | T3 €323.62 · R/R 1.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €307.78


## Edge, scénarios & sizing

- EV/risk : 0.016 | EV/share : €0.102 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 55 % | T2 35 % | T3 15 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 22.8 | side 72.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=18, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→55% · +2.0%→36% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.75% (p90 4.55%) · excursion haute méd. +1.2% / basse méd. −0.98%
- Profil de vol intra : ouverture 1.627% vs midi 0.623% vs clôture 0.744% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.109 ; mean-reverting — autocorr -0.037)_ ; drift intra méd. 0.104% ; recovery-V 30%
- **σ réalisé intraday** 1.786% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 52% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 326.8525 (VA 324.8275–327.2575 ; dernier close 327.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 18% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=154) : méd. -0.01% · baisse 50% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=155) : bas méd −0.48% (p90 −1.49%) · haut méd +0.18% · range méd 0.92%
- Excursion ouverture 15min (n=155) : bas méd −0.62% (p90 −1.61%) · haut méd +0.32% · range méd 1.17%
- Excursion ouverture 30min (n=155) : bas méd −0.64% (p90 −1.67%) · haut méd +0.44% · range méd 1.29%
- Excursion ouverture 60min (n=155) : bas méd −0.74% (p90 −1.8%) · haut méd +0.56% · range méd 1.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 327.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 68% (109/154) · gap 26% · délai 0.2min · rebond 37% (40/109) (MFE +0.78%)
   - −1.0% : fill 30min 43% · séance 55% (81/154) · gap 10% · délai 0.4min · rebond 40% (29/81) (MFE +0.63%)
   - −1.5% : fill 30min 29% · séance 47% (69/154) · gap 4% · délai 15.9min · rebond 44% (25/69) (MFE +0.91%)
   - −2.0% : fill 30min 14% · séance 37% (51/154) · gap 2% · délai 75.8min · rebond 50% (23/51) (MFE +0.97%)
   - −3.0% : fill 30min 4% · séance 18% (28/154) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 8% (13/154) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/154) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=188 jambes) : jambe baissière méd −1.09% (p90 −2.5%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (44/55) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (44 séances) :
      · −1.0% : fill 48% (19/44) · rebond 64% (10/19)
      · −2.0% : fill 19% (8/44) · rebond 66% (4/8)
      · −3.0% : fill 6% (4/44) · rebond 69% (3/4)
      · −4.0% : fill 1% (1/44) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/44) · rebond 0% (0/0)
   - **gap-up** (55 séances) :
      · −1.0% : fill 30% (18/55) · rebond 17% (3/18)
      · −2.0% : fill 22% (11/55) · rebond 43% (4/11)
      · −3.0% : fill 14% (7/55) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/55) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 53% en base · 72% si les 15 1res min sont vertes (67 cas) · 37% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=155) : COUDE à **44min** → P(séance verte=clôture>ouverture) 83% si début vert vs 28% si rouge (base 53% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **83%** · continue >prix actuel 66% ; creux résiduel méd -0.56% (q20 -1.4%) → **SL/trailing à −1.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +1.78% → **scale +1.28% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=87) : edge inversé — récupère vert seulement **28%** (continue à baisser 52%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.45%** (au-delà de la MAE q10 -2.45%), cible rebond +0.86% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-1.59% .. +1.57%] · haut q95 +1.94% · bas q05 -2.13%
   - 60min (n=155) : retour [-1.63% .. +2.14%] · haut q95 +2.35% · bas q05 -2.34%
   - 2h (n=155) : retour [-2.26% .. +2.16%] · haut q95 +2.55% · bas q05 -2.93%
   - 4h (n=155) : retour [-2.17% .. +2.19%] · haut q95 +3.16% · bas q05 -3.04%
   - 6h (n=155) : retour [-2.3% .. +2.91%] · haut q95 +3.39% · bas q05 -3.24%
   - session (n=155) : retour [-3.42% .. +3.28%] · haut q95 +3.66% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 23.5  _(survente)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist -3.447  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 13.4%
- **ATR** : 8.74 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.166  _(accumulation)_
- **Vol ratio** : 1.47  _(volume normal)_
- **Choppiness** : 38.9  _(transition)_
- **MA** : MA20 336.53 · MA50 316.44 · MA200 304.05  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 +1.6% · MA200 +5.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88889 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
