# NEX

**Generated** : 2026-07-29T00:07:52.498785+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €124.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot €124.90 (+0.3% vs entrée) · entrée €124.53 · stop €122.66 · T1 €125.89 · R/R 0.73  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.29 _(réel 5 s)_ (GBM -0.029) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €124.25–€124.80 (mid €124.53)
- Spot actuel : €124.90 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €122.66 (stop swing_plan-based (-1.62%))
- Targets : T1 €125.89 · R/R 0.73 | T2 €127.26 · R/R 1.46 | T3 €128.63 · R/R 2.19
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €122.66


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : €-0.054 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 25 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.1 | bear 12.9 | side 82.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.305% → cible +1.099% / stop −1.5%, p_fill 85%, n_eff≈32.5) : P(cible|rempli) **29%** · **EV/risk -0.290** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −0.396% → cible +2.457% / stop −1.228%, p_fill 89%, n_eff≈34.1) : P(cible|rempli) **25%** · **EV/risk -0.301** (×p_fill ; si rempli -0.41% du capital)
  - **deep** (entrée dip −0.502% → cible +3.474% / stop −1.737%, p_fill 89%, n_eff≈33.9) : P(cible|rempli) **30%** · **EV/risk -0.183** (×p_fill ; si rempli -0.36% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→56% · +2.0%→30% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 2.97% (p90 4.67%) · excursion haute méd. +1.14% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.69% vs midi 0.516% vs clôture 0.766% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 47% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.564% ; recovery-V 6%
- **σ réalisé intraday** 2.026% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 70% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 131.9075 (VA 131.1725–132.7475 ; dernier close 130.2)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 55% · **stop −1.88%** sous le fill (sous le bruit) · cible +1.17% · R/R 0.62 (high win-rate)
- Gaps overnight (n=140) : méd. 0.13% · baisse 39% (gap-down >1% 10% · >2% 2%)
- Excursion ouverture 5min (n=141) : bas méd −0.46% (p90 −1.94%) · haut méd +0.28% · range méd 1.01%
- Excursion ouverture 15min (n=141) : bas méd −0.59% (p90 −2.1%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=141) : bas méd −0.6% (p90 −2.31%) · haut méd +0.37% · range méd 1.41%
- Excursion ouverture 60min (n=141) : bas méd −0.75% (p90 −2.49%) · haut méd +0.51% · range méd 1.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 130.2 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 74% (101/140) · gap 25% · délai 0.4min · rebond 45% (49/101) (MFE +0.85%)
   - −1.0% : fill 30min 41% · séance 65% (84/140) · gap 10% · délai 9.4min · rebond 45% (39/84) (MFE +0.85%)
   - −1.5% : fill 30min 24% · séance 50% (62/140) · gap 3% · délai 60.7min · rebond 46% (29/62) (MFE +0.73%)
   - −2.0% : fill 30min 16% · séance 34% (46/140) · gap 2% · délai 71.1min · rebond 46% (24/46) (MFE +0.93%)
   - −3.0% : fill 30min 5% · séance 22% (28/140) · gap 1% · délai 126.7min · rebond 55% (16/28) (MFE +1.17%)
   - −4.0% : fill 30min 1% · séance 8% (10/140) · gap 1% · délai 277.7min · rebond 20% (4/10) (MFE +0.82%)
   - −5.0% : fill 30min 1% · séance 2% (4/140) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −0.95%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=279 jambes) : jambe baissière méd −1.05% (p90 −2.46%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (33 séances) :
      · −1.0% : fill 71% (22/33) · rebond 49% (12/22)
      · −2.0% : fill 35% (10/33) · rebond 50% (5/10)
      · −3.0% : fill 22% (6/33) · rebond 42% (2/6)
      · −4.0% : fill 5% (1/33) · rebond 0% (0/1)
      · −5.0% : fill 0% (0/33) · rebond 0% (0/0)
   - **gap-up** (63 séances) :
      · −1.0% : fill 50% (26/63) · rebond 41% (12/26)
      · −2.0% : fill 26% (11/63) · rebond 44% (6/11)
      · −3.0% : fill 15% (6/63) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/63) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/63) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 44% en base · 69% si les 15 1res min sont vertes (76 cas) · 15% si rouges (65 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=141) : COUDE à **28min** → P(séance verte=clôture>ouverture) 85% si début vert vs 14% si rouge (base 44% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 28min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.96% (q20 -1.74%) → **SL/trailing à −1.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +1.99% → **scale +1.23% / runner +1.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **14%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.85%** (au-delà de la MAE q10 -2.85%), cible rebond +0.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-2.11% .. +1.76%] · haut q95 +2.31% · bas q05 -2.84%
   - 60min (n=141) : retour [-2.68% .. +2.05%] · haut q95 +2.37% · bas q05 -3.19%
   - 2h (n=141) : retour [-3.55% .. +2.16%] · haut q95 +2.56% · bas q05 -3.74%
   - 4h (n=141) : retour [-3.15% .. +2.45%] · haut q95 +2.89% · bas q05 -3.88%
   - 6h (n=141) : retour [-3.36% .. +3.42%] · haut q95 +3.89% · bas q05 -4.15%
   - session (n=141) : retour [-3.52% .. +2.88%] · haut q95 +4.19% · bas q05 -4.48%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.8  _(momentum baissier)_
- **ADX** : 34.8  _(tendance etablie)_
- **MACD** : hist -0.256  _(bearish_recent)_
- **BB** : %B -0.12 · largeur 11.6%
- **ATR** : 3.74 (37.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.057  _(accumulation)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 47.6  _(transition)_
- **MA** : MA20 134.6 · MA50 145.9 · MA200 131.44  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -14.4% · MA200 -5.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90624 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
