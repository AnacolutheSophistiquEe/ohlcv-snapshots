# SRT3

**Generated** : 2026-07-23T00:02:07.504922+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €224.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot €224.90 (+0.4% vs entrée) · entrée €224.10 · stop €218.50 · T1 €228.36 · R/R 0.76  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk -0.07 _(réel 5 s)_ (GBM 0.081) · ¼-Kelly 0.022 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €223.30–€224.90 (mid €224.10)
- Spot actuel : €224.90 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €218.50 (stop swing_plan-based (-2.9%))
- Targets : T1 €228.36 · R/R 0.76 | T2 €232.61 · R/R 1.52 | T3 €236.87 · R/R 2.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €218.50


## Edge, scénarios & sizing

- EV/risk : 0.081 | EV/share : €0.455 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 15 % | T3 10 %
- Kelly (position) : f* 0.087 | ¼-Kelly 0.022 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.2 | bear 33.8 | side 54.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.359% → cible +1.9% / stop −2.5%, p_fill 87%, n_eff≈34.5) : P(cible|rempli) **29%** · **EV/risk -0.070** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −0.793% → cible +4.248% / stop −2.124%, p_fill 75%, n_eff≈31.0) : P(cible|rempli) **24%** · **EV/risk -0.182** (×p_fill ; si rempli -0.51% du capital)
  - **deep** (entrée dip −1.161% → cible +6.008% / stop −3.004%, p_fill 83%, n_eff≈32.5) : P(cible|rempli) **30%** · **EV/risk -0.114** (×p_fill ; si rempli -0.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→48% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.65% (p90 6.82%) · excursion haute méd. +1.94% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.051% vs midi 0.847% vs clôture 0.994% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; neutre — autocorr -0.005)_ ; drift intra méd. -0.067% ; recovery-V 28%
- **σ réalisé intraday** 2.728% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 58% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 234.5613 (VA 217.5663–235.3338 ; dernier close 218.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 59% · rebond 70% · **stop −2.5%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.66 (high win-rate)
- Gaps overnight (n=159) : méd. -0.13% · baisse 55% (gap-down >1% 18% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.37% (p90 −1.77%) · haut méd +0.48% · range méd 1.22%
- Excursion ouverture 15min (n=160) : bas méd −0.53% (p90 −1.87%) · haut méd +0.63% · range méd 1.55%
- Excursion ouverture 30min (n=160) : bas méd −0.59% (p90 −2.01%) · haut méd +0.71% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.68% (p90 −2.36%) · haut méd +0.77% · range méd 1.88%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 218.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 78% (126/159) · gap 32% · délai 0.2min · rebond 54% (61/126) (MFE +1.12%)
   - −1.0% : fill 30min 46% · séance 66% (106/159) · gap 18% · délai 0.3min · rebond 62% (63/106) (MFE +1.33%)
   - −1.5% : fill 30min 36% · séance 59% (93/159) · gap 9% · délai 4.3min · rebond 70% (59/93) (MFE +1.66%)
   - −2.0% : fill 30min 23% · séance 44% (72/159) · gap 5% · délai 21.2min · rebond 59% (44/72) (MFE +1.5%)
   - −3.0% : fill 30min 7% · séance 22% (42/159) · gap 2% · délai 184.1min · rebond 54% (25/42) (MFE +1.52%)
   - −4.0% : fill 30min 5% · séance 12% (21/159) · gap 1% · délai 78.1min · rebond 72% (16/21) (MFE +1.69%)
   - −5.0% : fill 30min 1% · séance 8% (11/159) · gap 1% · délai 148.6min · rebond 56% (8/11) (MFE +2.14%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.87%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.77%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.25% (p90 −1.79%) → stop au-delà de −1.22% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=409 jambes) : jambe baissière méd −1.04% (p90 −2.57%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (78 séances) :
      · −1.0% : fill 86% (66/78) · rebond 72% (44/66)
      · −2.0% : fill 57% (44/78) · rebond 65% (29/44)
      · −3.0% : fill 34% (30/78) · rebond 49% (17/30)
      · −4.0% : fill 16% (16/78) · rebond 71% (12/16)
      · −5.0% : fill 8% (7/78) · rebond 92% (6/7)
   - **flat** (35 séances) :
      · −1.0% : fill 60% (20/35) · rebond 43% (9/20)
      · −2.0% : fill 49% (15/35) · rebond 48% (7/15)
      · −3.0% : fill 23% (7/35) · rebond 66% (5/7)
      · −4.0% : fill 17% (4/35) · rebond 70% (3/4)
      · −5.0% : fill 17% (4/35) · rebond 24% (2/4)
   - **gap-up** (46 séances) :
      · −1.0% : fill 41% (20/46) · rebond 52% (10/20)
      · −2.0% : fill 21% (13/46) · rebond 55% (8/13)
      · −3.0% : fill 5% (5/46) · rebond 52% (3/5)
      · −4.0% : fill 1% (1/46) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/46) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 60% si les 15 1res min sont vertes (90 cas) · 40% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:16** → P(séance verte=clôture>ouverture) 67% si début vert vs 33% si rouge (base 51% · écart 34 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **67%** · continue >prix actuel 44% ; creux résiduel méd -1.27% (q20 -2.35%) → **SL/trailing à −2.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.5% → **scale +1.13% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **33%** (continue à baisser 57%) → **RÉDUIRE ~67%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.02%** (au-delà de la MAE q10 -4.02%), cible rebond +1.34% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.34% .. +2.13%] · haut q95 +2.67% · bas q05 -2.84%
   - 60min (n=160) : retour [-2.31% .. +2.33%] · haut q95 +2.86% · bas q05 -3.27%
   - 2h (n=160) : retour [-2.21% .. +2.69%] · haut q95 +3.12% · bas q05 -3.79%
   - 4h (n=160) : retour [-2.82% .. +2.82%] · haut q95 +3.39% · bas q05 -3.84%
   - 6h (n=160) : retour [-2.95% .. +3.56%] · haut q95 +4.2% · bas q05 -4.79%
   - session (n=160) : retour [-3.81% .. +4.86%] · haut q95 +6.21% · bas q05 -5.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist -1.399  _(bearish_recent)_
- **BB** : %B 0.29 · largeur 17.1%
- **ATR** : 11.19 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.024  _(neutre)_
- **Vol ratio** : 0.85  _(volume normal)_
- **Choppiness** : 48.7  _(transition)_
- **MA** : MA20 233.46 · MA50 231.23 · MA200 231.66  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 -2.7% · MA200 -2.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90607 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
