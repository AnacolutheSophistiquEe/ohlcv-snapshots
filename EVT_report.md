# EVT

**Generated** : 2026-07-08T00:04:45.064600+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €5.05  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €5.05 (+1.2% vs entrée) · entrée €4.99 · stop €4.92 · T1 €5.11 · R/R 1.71  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.015 _(réel 5 s)_ (GBM 0.144) · ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 181 % hors [0,100] (R² max 0.56). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €4.96–€5.01 (mid €4.99)
- Spot actuel : €5.05 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €4.92 (stop swing_plan-based (-2.59%))
- Targets : T1 €5.11 · R/R 1.71 | T2 €5.23 · R/R 3.43 | T3 €5.36 · R/R 5.29
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.92


## Edge, scénarios & sizing

- EV/risk : 0.144 | EV/share : €0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 27 % | T3 17 %
- Kelly (position) : f* 0.049 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 20.5 | bear 6.4 | side 73.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 283.0 (= 56 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.622% → cible +1.111% / stop −3.5%, p_fill 79%, n_eff≈32.0) : P(cible|rempli) **80%** · **EV/risk +0.083** (×p_fill ; si rempli +0.36% du capital)
  - **swing** (entrée dip −1.365% → cible +2.483% / stop −1.242%, p_fill 58%, n_eff≈27.7) : P(cible|rempli) **35%** · **EV/risk -0.015** (×p_fill ; si rempli -0.03% du capital)
  - **deep** (entrée dip −2.111% → cible +3.512% / stop −1.756%, p_fill 69%, n_eff≈31.3) : P(cible|rempli) **34%** · **EV/risk -0.034** (×p_fill ; si rempli -0.09% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→46% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.43% (p90 6.71%) · excursion haute méd. +1.93% / basse méd. −1.83%
- Profil de vol intra : ouverture 2.693% vs midi 1.226% vs clôture 1.241% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.082 ; mean-reverting — autocorr -0.123)_ ; drift intra méd. 0.44% ; recovery-V 53%
- **σ réalisé intraday** 2.978% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 64% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 5.1473 (VA 5.1419–5.1987 ; dernier close 5.166)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 30% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.58% (p90 −2.13%) · haut méd +0.76% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.77% (p90 −2.32%) · haut méd +0.89% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.73%) · haut méd +0.97% · range méd 2.19%
- Excursion ouverture 60min (n=160) : bas méd −0.91% (p90 −2.89%) · haut méd +1.03% · range méd 2.36%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 5.166 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 83% (132/159) · gap 34% · délai 0.3min · rebond 64% (87/132) (MFE +1.43%)
   - −1.0% : fill 30min 51% · séance 76% (120/159) · gap 21% · délai 1.0min · rebond 68% (78/120) (MFE +1.52%)
   - −1.5% : fill 30min 34% · séance 56% (95/159) · gap 15% · délai 12.1min · rebond 63% (60/95) (MFE +1.39%)
   - −2.0% : fill 30min 28% · séance 45% (76/159) · gap 11% · délai 9.2min · rebond 61% (49/76) (MFE +1.37%)
   - −3.0% : fill 30min 14% · séance 30% (54/159) · gap 5% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 7% · séance 17% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.18%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −2.03%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.73%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=789 jambes) : jambe baissière méd −1.05% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 94% (61/64) · rebond 67% (36/61)
      · −2.0% : fill 64% (44/64) · rebond 63% (28/44)
      · −3.0% : fill 45% (34/64) · rebond 76% (26/34)
      · −4.0% : fill 29% (21/64) · rebond 65% (15/21)
      · −5.0% : fill 16% (14/64) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 85% (30/39) · rebond 82% (24/30)
      · −2.0% : fill 42% (15/39) · rebond 57% (10/15)
      · −3.0% : fill 21% (8/39) · rebond 94% (7/8)
      · −4.0% : fill 11% (3/39) · rebond 52% (1/3)
      · −5.0% : fill 5% (2/39) · rebond 72% (1/2)
   - **gap-up** (56 séances) :
      · −1.0% : fill 49% (29/56) · rebond 56% (18/29)
      · −2.0% : fill 26% (17/56) · rebond 60% (11/17)
      · −3.0% : fill 19% (12/56) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/56) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 61% en base · 72% si les 15 1res min sont vertes (79 cas) · 49% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:05** → P(séance verte=clôture>ouverture) 81% si début vert vs 37% si rouge (base 61% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -1.44% (q20 -2.31%) → **SL/trailing à −2.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.17% / q75 +2.38% → **scale +1.17% / runner +2.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **37%** (continue à baisser 44%) → **RÉDUIRE ~63%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.72%** (au-delà de la MAE q10 -3.72%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.37% .. +2.43%] · haut q95 +3.58% · bas q05 -2.87%
   - 60min (n=160) : retour [-2.78% .. +3.1%] · haut q95 +4.35% · bas q05 -3.33%
   - 2h (n=160) : retour [-3.0% .. +3.2%] · haut q95 +4.53% · bas q05 -3.86%
   - 4h (n=160) : retour [-2.95% .. +3.02%] · haut q95 +4.53% · bas q05 -3.94%
   - 6h (n=160) : retour [-3.35% .. +3.26%] · haut q95 +4.7% · bas q05 -4.33%
   - session (n=160) : retour [-4.23% .. +4.09%] · haut q95 +5.83% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.9  _(momentum haussier)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist 0.047  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 16.4%
- **ATR** : 0.17 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.139  _(accumulation)_
- **Vol ratio** : 0.44  _(volume atone)_
- **Choppiness** : 47.2  _(transition)_
- **MA** : MA20 4.85 · MA50 4.97 · MA200 5.53  _(prix > MA20)_
- **Dist MA** : MA20 +4.3% · MA50 +1.8% · MA200 -8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93521 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
