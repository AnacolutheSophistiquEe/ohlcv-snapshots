# NEX

**Generated** : 2026-07-28T00:06:50.941162+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €130.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €130.30 (+2.5% vs entrée) · entrée €127.16 · stop €125.67 · T1 €130.14 · R/R 2.0  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.21 _(réel 5 s)_ (GBM 0.067) · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €126.56–€127.76 (mid €127.16)
- Spot actuel : €130.30 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : €125.67 (stop swing_plan-based (-3.56%))
- Targets : T1 €130.14 · R/R 2.0 | T2 €133.13 · R/R 4.01 | T3 €136.11 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €125.67


## Edge, scénarios & sizing

- EV/risk : 0.067 | EV/share : €0.100 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 8 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 71.8 | bear 9.3 | side 18.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.096% → cible +1.049% / stop −1.5%, p_fill 55%, n_eff≈22.1) : P(cible|rempli) **27%** · **EV/risk -0.215** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −2.415% → cible +2.347% / stop −1.173%, p_fill 53%, n_eff≈22.5) : P(cible|rempli) **23%** · **EV/risk -0.210** (×p_fill ; si rempli -0.47% du capital)
  - **deep** (entrée dip −3.723% → cible +3.318% / stop −1.659%, p_fill 52%, n_eff≈19.7) : P(cible|rempli) **18%** · **EV/risk -0.263** (×p_fill ; si rempli -0.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→57% · +2.0%→30% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 2.97% (p90 4.67%) · excursion haute méd. +1.16% / basse méd. −0.99%
- Profil de vol intra : ouverture 1.693% vs midi 0.525% vs clôture 0.76% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 46% · recovery-V 16%)_
- **Régime intraday** : **chop** _(efficiency 0.11 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.505% ; recovery-V 6%
- **σ réalisé intraday** 2.035% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 69% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 133.1238 (VA 132.8938–133.6988 ; dernier close 132.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 22% · rebond 55% · **stop −1.88%** sous le fill (sous le bruit) · cible +1.17% · R/R 0.62 (high win-rate)
- Gaps overnight (n=139) : méd. 0.13% · baisse 40% (gap-down >1% 11% · >2% 2%)
- Excursion ouverture 5min (n=140) : bas méd −0.5% (p90 −1.94%) · haut méd +0.3% · range méd 1.02%
- Excursion ouverture 15min (n=140) : bas méd −0.59% (p90 −2.12%) · haut méd +0.37% · range méd 1.29%
- Excursion ouverture 30min (n=140) : bas méd −0.6% (p90 −2.34%) · haut méd +0.43% · range méd 1.41%
- Excursion ouverture 60min (n=140) : bas méd −0.7% (p90 −2.49%) · haut méd +0.56% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 132.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 73% (100/139) · gap 26% · délai 0.4min · rebond 46% (49/100) (MFE +0.87%)
   - −1.0% : fill 30min 42% · séance 64% (83/139) · gap 11% · délai 8.8min · rebond 46% (39/83) (MFE +0.93%)
   - −1.5% : fill 30min 25% · séance 49% (61/139) · gap 3% · délai 23.0min · rebond 48% (29/61) (MFE +0.76%)
   - −2.0% : fill 30min 16% · séance 33% (45/139) · gap 2% · délai 36.7min · rebond 48% (24/45) (MFE +0.99%)
   - −3.0% : fill 30min 5% · séance 22% (28/139) · gap 1% · délai 126.7min · rebond 55% (16/28) (MFE +1.17%)
   - −4.0% : fill 30min 1% · séance 8% (10/139) · gap 1% · délai 277.7min · rebond 20% (4/10) (MFE +0.82%)
   - −5.0% : fill 30min 1% · séance 2% (4/139) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.1% (p90 −0.95%) → stop au-delà de −0.68% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.9%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.19% (p90 −1.32%) → stop au-delà de −0.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=276 jambes) : jambe baissière méd −1.04% (p90 −2.46%) · ~6.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (32 séances) :
      · −1.0% : fill 69% (21/32) · rebond 54% (12/21)
      · −2.0% : fill 30% (9/32) · rebond 63% (5/9)
      · −3.0% : fill 24% (6/32) · rebond 42% (2/6)
      · −4.0% : fill 6% (1/32) · rebond 0% (0/1)
      · −5.0% : fill 0% (0/32) · rebond 0% (0/0)
   - **gap-up** (63 séances) :
      · −1.0% : fill 50% (26/63) · rebond 41% (12/26)
      · −2.0% : fill 26% (11/63) · rebond 44% (6/11)
      · −3.0% : fill 15% (6/63) · rebond 77% (5/6)
      · −4.0% : fill 4% (2/63) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/63) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 45% en base · 72% si les 15 1res min sont vertes (75 cas) · 15% si rouges (65 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=140) : COUDE à **28min** → P(séance verte=clôture>ouverture) 85% si début vert vs 15% si rouge (base 45% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 28min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **85%** · continue >prix actuel 57% ; creux résiduel méd -0.96% (q20 -1.74%) → **SL/trailing à −1.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +1.99% → **scale +1.23% / runner +1.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **15%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.91%** (au-delà de la MAE q10 -2.91%), cible rebond +0.98% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-2.12% .. +1.77%] · haut q95 +2.32% · bas q05 -2.84%
   - 60min (n=140) : retour [-2.7% .. +2.05%] · haut q95 +2.38% · bas q05 -3.19%
   - 2h (n=140) : retour [-3.56% .. +2.16%] · haut q95 +2.59% · bas q05 -3.74%
   - 4h (n=140) : retour [-3.18% .. +2.48%] · haut q95 +2.9% · bas q05 -3.89%
   - 6h (n=140) : retour [-3.38% .. +3.44%] · haut q95 +3.93% · bas q05 -4.17%
   - session (n=140) : retour [-3.53% .. +2.88%] · haut q95 +4.19% · bas q05 -4.5%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.4% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.94%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.2  _(momentum baissier)_
- **ADX** : 33.3  _(tendance etablie)_
- **MACD** : hist 0.138  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 11.5%
- **ATR** : 3.57 (31.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.094  _(accumulation)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 60.6  _(transition)_
- **MA** : MA20 135.62 · MA50 146.43 · MA200 131.38  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -11.0% · MA200 -0.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89430 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
