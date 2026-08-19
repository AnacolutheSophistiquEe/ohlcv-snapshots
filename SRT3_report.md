# SRT3

**Generated** : 2026-08-19T21:37:07.656324+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €234.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €234.70 (+1.1% vs entrée) · entrée €232.09 · stop €228.61 · T1 €234.27 · R/R 0.63  
> ↳ P(T1 av. stop) 42 % _(réel 5 s)_ · EV/risk -0.098 _(réel 5 s)_ (GBM 0.057) · ¼-Kelly 0.032 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €231.66–€232.53 (mid €232.09)
- Spot actuel : €234.70 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : €228.61 (stop swing_plan-based (-5.48%))
- Targets : T1 €234.27 · R/R 0.63 | T2 €236.45 · R/R 1.25 | T3 €238.63 · R/R 1.88
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €228.61


## Edge, scénarios & sizing

- EV/risk : 0.057 | EV/share : €0.198 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 69 % | T2 44 % | T3 25 %
- Kelly (position) : f* 0.129 | ¼-Kelly 0.032 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.4 | bear 82.1 | side 6.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 235.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.107% → cible +0.939% / stop −1.5%, p_fill 59%, n_eff≈23.4) : P(cible|rempli) **42%** · **EV/risk -0.098** (×p_fill ; si rempli -0.25% du capital)
  - **swing** (entrée dip −2.446% → cible +2.1% / stop −3.11%, p_fill 39%, n_eff≈18.6) : P(cible|rempli) **76%** · **EV/risk +0.088** (×p_fill ; si rempli +0.71% du capital)
  - **deep** (entrée dip −3.779% → cible +2.97% / stop −4.73%, p_fill 43%, n_eff≈17.6) : P(cible|rempli) **70%** · **EV/risk +0.044** (×p_fill ; si rempli +0.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→48% · +3.0%→25% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.49% (p90 6.59%) · excursion haute méd. +1.89% / basse méd. −1.55%
- Profil de vol intra : ouverture 2.106% vs midi 0.863% vs clôture 0.98% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.1 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.001% ; recovery-V 26%
- **σ réalisé intraday** 2.615% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 73% / whipsaw 44%
- POC intraday (dernière séance, temps-au-prix) : 235.8194 (VA 235.4719–238.4256 ; dernier close 236.35)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 56% · rebond 72% · **stop −2.38%** sous le fill (sous le bruit) · cible +1.67% · R/R 0.7 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 48% (gap-down >1% 13% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.37% (p90 −1.86%) · haut méd +0.57% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.53% (p90 −1.97%) · haut méd +0.66% · range méd 1.51%
- Excursion ouverture 30min (n=160) : bas méd −0.58% (p90 −2.24%) · haut méd +0.82% · range méd 1.72%
- Excursion ouverture 60min (n=160) : bas méd −0.68% (p90 −2.6%) · haut méd +0.87% · range méd 1.82%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 236.35 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 76% (124/159) · gap 24% · délai 0.3min · rebond 56% (65/124) (MFE +1.2%)
   - −1.0% : fill 30min 40% · séance 64% (104/159) · gap 13% · délai 2.8min · rebond 59% (59/104) (MFE +1.36%)
   - −1.5% : fill 30min 34% · séance 56% (95/159) · gap 6% · délai 5.0min · rebond 72% (61/95) (MFE +1.67%)
   - −2.0% : fill 30min 20% · séance 39% (74/159) · gap 4% · délai 32.2min · rebond 66% (46/74) (MFE +1.96%)
   - −3.0% : fill 30min 6% · séance 17% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 10% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.07%) → stop au-delà de −1.15% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.16% (p90 −2.4%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.73%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=435 jambes) : jambe baissière méd −1.05% (p90 −2.51%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (69 séances) :
      · −1.0% : fill 78% (57/69) · rebond 68% (36/57)
      · −2.0% : fill 50% (42/69) · rebond 64% (27/42)
      · −3.0% : fill 30% (28/69) · rebond 48% (15/28)
      · −4.0% : fill 14% (15/69) · rebond 71% (11/15)
      · −5.0% : fill 7% (7/69) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 68% (21/34) · rebond 54% (10/21)
      · −2.0% : fill 47% (16/34) · rebond 62% (8/16)
      · −3.0% : fill 16% (6/34) · rebond 66% (4/6)
      · −4.0% : fill 12% (4/34) · rebond 70% (3/4)
      · −5.0% : fill 12% (4/34) · rebond 24% (2/4)
   - **gap-up** (56 séances) :
      · −1.0% : fill 47% (26/56) · rebond 50% (13/26)
      · −2.0% : fill 24% (16/56) · rebond 77% (11/16)
      · −3.0% : fill 7% (6/56) · rebond 78% (4/6)
      · −4.0% : fill 4% (2/56) · rebond 100% (2/2)
      · −5.0% : fill 4% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 56% si les 15 1res min sont vertes (90 cas) · 39% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **8min** → P(séance verte=clôture>ouverture) 57% si début vert vs 38% si rouge (base 49% · écart 19 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **57%** · continue >prix actuel 46% ; creux résiduel méd -1.42% (q20 -2.39%) → **SL/trailing à −2.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.35% → **scale +1.34% / runner +2.35%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **38%** (continue à baisser 55%) → **RÉDUIRE ~61%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.22%** (au-delà de la MAE q10 -5.22%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.95% .. +2.17%] · haut q95 +2.64% · bas q05 -3.4%
   - 60min (n=160) : retour [-3.14% .. +2.36%] · haut q95 +2.87% · bas q05 -3.78%
   - 2h (n=160) : retour [-2.21% .. +2.53%] · haut q95 +2.95% · bas q05 -3.83%
   - 4h (n=160) : retour [-2.55% .. +2.29%] · haut q95 +3.3% · bas q05 -3.84%
   - 6h (n=160) : retour [-2.67% .. +2.99%] · haut q95 +3.73% · bas q05 -4.95%
   - session (n=160) : retour [-3.66% .. +4.16%] · haut q95 +5.66% · bas q05 -5.17%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 61.3  _(momentum haussier)_
- **ADX** : 12.5  _(pas de tendance nette)_
- **MACD** : hist 0.412  _(pas de croisement recent)_
- **BB** : %B 0.71 · largeur 12.1%
- **ATR** : 7.12 (22.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.022  _(neutre)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 58.7  _(transition)_
- **MA** : MA20 228.75 · MA50 229.61 · MA200 231.86  _(prix > MA20)_
- **Dist MA** : MA20 +2.6% · MA50 +2.2% · MA200 +1.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91539 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
