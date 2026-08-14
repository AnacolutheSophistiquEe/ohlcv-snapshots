# SOFI

**Generated** : 2026-08-14T00:32:17.146440+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.43  

> 🟡 **WAIT-FOR-DIP** — spot +3.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.43 (+3.5% vs entrée) · entrée $17.80 · stop $17.09 · T1 $18.20 · R/R 0.56  
> ↳ P(T1 av. stop) 78 % · EV/risk 0.115 · ¼-Kelly 0.039 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.0% cohérent avec le bruit 5 s (EV-optimal ≈ −4.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.72–$17.88 (mid $17.80)
- Spot actuel : $18.43 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : $17.09 (stop swing_plan-based (-12.24%))
- Targets : T1 $18.20 · R/R 0.56 | T2 $18.60 · R/R 1.13 | T3 $19.00 · R/R 1.69
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.09


## Edge, scénarios & sizing

- EV/risk : 0.011 | EV/share : $0.008 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 15 % | T3 11 %
- Kelly (position) : f* 0.157 | ¼-Kelly 0.039 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 79.1 | bear 11.6 | side 9.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 387.0 (= 21 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.406% → cible +2.246% / stop −4.0%, p_fill 18%, n_eff≈9.5) : P(cible|rempli) **44%** · **EV/risk +0.031** (×p_fill ; si rempli +0.67% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→68% · +2.0%→48% · +3.0%→36% · +5.0%→11% · +8.0%→1%
- Range intraday médian 4.38% (p90 7.29%) · excursion haute méd. +1.84% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.992% vs midi 0.899% vs clôture 0.997% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 15% · trend ↑2%/↓0% ; spike-down 66% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; neutre — autocorr -0.026)_ ; drift intra méd. 0.207% ; recovery-V 17%
- **σ réalisé intraday** 2.75% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 17.9532 (VA 17.8372–18.1127 ; dernier close 17.98)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 71% · **stop −2.96%** sous le fill (sous le bruit) · cible +1.86% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 44% (gap-down >1% 26% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.66%) · haut méd +0.72% · range méd 1.65%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −2.93%) · haut méd +0.96% · range méd 2.24%
- Excursion ouverture 30min (n=160) : bas méd −1.17% (p90 −3.25%) · haut méd +1.12% · range méd 2.69%
- Excursion ouverture 60min (n=160) : bas méd −1.49% (p90 −3.77%) · haut méd +1.22% · range méd 3.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.98 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (121/159) · gap 31% · délai 0.0min · rebond 51% (64/121) (MFE +1.07%)
   - −1.0% : fill 30min 54% · séance 67% (111/159) · gap 26% · délai 1.0min · rebond 60% (69/111) (MFE +1.23%)
   - −1.5% : fill 30min 46% · séance 64% (103/159) · gap 19% · délai 9.8min · rebond 68% (67/103) (MFE +1.44%)
   - −2.0% : fill 30min 37% · séance 51% (80/159) · gap 10% · délai 4.9min · rebond 71% (55/80) (MFE +1.86%)
   - −3.0% : fill 30min 16% · séance 35% (58/159) · gap 4% · délai 31.4min · rebond 66% (40/58) (MFE +1.57%)
   - −4.0% : fill 30min 10% · séance 21% (39/159) · gap 3% · délai 41.0min · rebond 57% (25/39) (MFE +1.46%)
   - −5.0% : fill 30min 4% · séance 8% (18/159) · gap 2% · délai 26.7min · rebond 40% (10/18) (MFE +0.71%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −1.89%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.71%) → stop au-delà de −1.06% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=660 jambes) : jambe baissière méd −1.09% (p90 −2.77%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 97% (64/65) · rebond 62% (40/64)
      · −2.0% : fill 86% (55/65) · rebond 73% (40/55)
      · −3.0% : fill 68% (44/65) · rebond 73% (33/44)
      · −4.0% : fill 40% (29/65) · rebond 65% (21/29)
      · −5.0% : fill 20% (14/65) · rebond 38% (8/14)
   - **flat** (23 séances) :
      · −1.0% : fill 60% (14/23) · rebond 35% (6/14)
      · −2.0% : fill 48% (9/23) · rebond 69% (5/9)
      · −3.0% : fill 30% (6/23) · rebond 57% (3/6)
      · −4.0% : fill 13% (3/23) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/23) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 45% (33/71) · rebond 65% (23/33)
      · −2.0% : fill 24% (16/71) · rebond 66% (10/16)
      · −3.0% : fill 10% (8/71) · rebond 39% (4/8)
      · −4.0% : fill 8% (7/71) · rebond 20% (3/7)
      · −5.0% : fill 1% (3/71) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 60% si les 15 1res min sont vertes (71 cas) · 26% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 79% si début vert vs 12% si rouge (base 42% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 228min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -1.51% (q20 -2.82%) → **SL/trailing à −2.82%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.9% / q75 +2.86% → **scale +1.9% / runner +2.86%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **12%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.02%** (au-delà de la MAE q10 -3.02%), cible rebond +1.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.86% .. +3.63%] · haut q95 +4.01% · bas q05 -3.55%
   - 60min (n=160) : retour [-3.11% .. +3.59%] · haut q95 +4.37% · bas q05 -4.0%
   - 2h (n=160) : retour [-3.58% .. +3.76%] · haut q95 +4.95% · bas q05 -4.55%
   - 4h (n=160) : retour [-3.79% .. +4.81%] · haut q95 +5.73% · bas q05 -5.03%
   - 6h (n=160) : retour [-4.48% .. +4.42%] · haut q95 +6.51% · bas q05 -5.08%
   - session (n=160) : retour [-4.42% .. +5.43%] · haut q95 +6.62% · bas q05 -5.13%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 62.9  _(momentum haussier)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist 0.123  _(pas de croisement recent)_
- **BB** : %B 0.79 · largeur 20.9%
- **ATR** : 0.87 (20.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.062  _(accumulation)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 42.6  _(transition)_
- **MA** : MA20 17.38 · MA50 17.46 · MA200 20.88  _(prix > MA20)_
- **Dist MA** : MA20 +6.0% · MA50 +5.6% · MA200 -11.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84652 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
