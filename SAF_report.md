# SAF

**Generated** : 2026-07-30T00:06:40.764552+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €339.80  

> 🟡 **WAIT-FOR-DIP** — spot +8.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €339.80 (+8.4% vs entrée) · entrée €313.53 · stop €310.01 · T1 €320.57 · R/R 2.0  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.051 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 130 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €312.12–€314.94 (mid €313.53)
- Spot actuel : €339.80 (+8.4% au-dessus de la zone — repli à attendre)
- Stop : €310.01 (stop swing_plan-based (-8.77%))
- Targets : T1 €320.57 · R/R 2.0 | T2 €327.62 · R/R 4.0 | T3 €334.66 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €310.01


## Edge, scénarios & sizing

- EV/risk : 0.051 | EV/share : €0.181 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 19 % | T3 12 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 39.5 | side 55.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 340.0 (= 1 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→54% · +2.0%→35% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.72% (p90 4.62%) · excursion haute méd. +1.13% / basse méd. −1.01%
- Profil de vol intra : ouverture 1.707% vs midi 0.623% vs clôture 0.752% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.106 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. 0.104% ; recovery-V 25%
- **σ réalisé intraday** 1.922% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 47% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 341.4475 (VA 340.6375–343.0675 ; dernier close 340.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 18% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=158) : méd. 0.0% · baisse 50% (gap-down >1% 10% · >2% 1%)
- Excursion ouverture 5min (n=159) : bas méd −0.51% (p90 −1.82%) · haut méd +0.14% · range méd 0.94%
- Excursion ouverture 15min (n=159) : bas méd −0.62% (p90 −1.92%) · haut méd +0.26% · range méd 1.2%
- Excursion ouverture 30min (n=159) : bas méd −0.64% (p90 −1.93%) · haut méd +0.5% · range méd 1.32%
- Excursion ouverture 60min (n=159) : bas méd −0.74% (p90 −2.0%) · haut méd +0.56% · range méd 1.55%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 340.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 68% (112/158) · gap 24% · délai 0.2min · rebond 40% (42/112) (MFE +0.81%)
   - −1.0% : fill 30min 44% · séance 55% (83/158) · gap 10% · délai 0.4min · rebond 41% (30/83) (MFE +0.63%)
   - −1.5% : fill 30min 31% · séance 47% (71/158) · gap 4% · délai 7.5min · rebond 45% (26/71) (MFE +0.91%)
   - −2.0% : fill 30min 14% · séance 36% (52/158) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 18% (29/158) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 8% (13/158) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/158) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −0.91%) → stop au-delà de −0.75% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.16% (p90 −0.83%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=197 jambes) : jambe baissière méd −1.1% (p90 −2.52%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (44/55) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (46 séances) :
      · −1.0% : fill 48% (20/46) · rebond 56% (10/20)
      · −2.0% : fill 22% (9/46) · rebond 75% (5/9)
      · −3.0% : fill 11% (5/46) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/46) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/46) · rebond 0% (0/0)
   - **gap-up** (57 séances) :
      · −1.0% : fill 32% (19/57) · rebond 31% (4/19)
      · −2.0% : fill 20% (11/57) · rebond 43% (4/11)
      · −3.0% : fill 12% (7/57) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/57) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 53% en base · 75% si les 15 1res min sont vertes (69 cas) · 34% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=159) : COUDE à **44min** → P(séance verte=clôture>ouverture) 84% si début vert vs 26% si rouge (base 53% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **84%** · continue >prix actuel 64% ; creux résiduel méd -0.56% (q20 -1.4%) → **SL/trailing à −1.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.44% / q75 +1.85% → **scale +1.44% / runner +1.85%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **26%** (continue à baisser 49%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.44%** (au-delà de la MAE q10 -2.44%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-1.64% .. +1.57%] · haut q95 +1.96% · bas q05 -2.37%
   - 60min (n=159) : retour [-1.83% .. +2.12%] · haut q95 +2.22% · bas q05 -2.75%
   - 2h (n=159) : retour [-2.52% .. +2.15%] · haut q95 +2.54% · bas q05 -3.09%
   - 4h (n=159) : retour [-2.16% .. +2.19%] · haut q95 +2.99% · bas q05 -3.49%
   - 6h (n=159) : retour [-2.26% .. +2.91%] · haut q95 +3.3% · bas q05 -3.96%
   - session (n=159) : retour [-3.37% .. +3.01%] · haut q95 +3.65% · bas q05 -4.11%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 49.8  _(neutre)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist -0.28  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 12.9%
- **ATR** : 9.2 (66.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.078  _(accumulation)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 335.61 · MA50 321.56 · MA200 304.85  _(prix > MA20)_
- **Dist MA** : MA20 +1.2% · MA50 +5.7% · MA200 +11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88284 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
