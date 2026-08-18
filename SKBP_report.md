# 326030

**Generated** : 2026-08-18T21:56:52.129257+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩84500.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩84500.00 (+1.9% vs entrée) · entrée ₩82923.33 · stop ₩78823.33 · T1 ₩85424.83 · R/R 0.61  
> ↳ P(T1 av. stop) 67 % _(réel 5 s)_ · EV/risk 0.04 _(réel 5 s)_ (GBM -0.046) · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩82423.03–₩83423.63 (mid ₩82923.33)
- Spot actuel : ₩84500.00 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : ₩78823.33 (stop swing_plan-based (-6.72%))
- Targets : T1 ₩85424.83 · R/R 0.61 | T2 ₩87926.32 · R/R 1.22 | T3 ₩90427.82 · R/R 1.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩78823.33


## Edge, scénarios & sizing

- EV/risk : -0.046 | EV/share : ₩-187.440 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 32 % | T3 16 %
- Kelly (position) : f* 0.03 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 30.6 | side 64.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.853% → cible +1.349% / stop −1.5%, p_fill 73%, n_eff≈30.3) : P(cible|rempli) **45%** · **EV/risk -0.072** (×p_fill ; si rempli -0.15% du capital)
  - **swing** (entrée dip −1.868% → cible +3.017% / stop −4.944%, p_fill 61%, n_eff≈29.3) : P(cible|rempli) **67%** · **EV/risk +0.040** (×p_fill ; si rempli +0.33% du capital)
  - **deep** (entrée dip −2.882% → cible +4.266% / stop −7.494%, p_fill 72%, n_eff≈30.9) : P(cible|rempli) **69%** · **EV/risk +0.089** (×p_fill ; si rempli +0.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→70% · +2.0%→50% · +3.0%→36% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.47% (p90 7.69%) · excursion haute méd. +2.03% / basse méd. −2.12%
- Profil de vol intra : ouverture 2.975% vs midi 0.918% vs clôture 0.907% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (155 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 13% · trend ↑1%/↓1% ; spike-down 58% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; mean-reverting — autocorr -0.121)_ ; drift intra méd. 0.196% ; recovery-V 33%
- **σ réalisé intraday** 3.354% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 54% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 86392.5 (VA 86132.5–86912.5 ; dernier close 86700.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 68% · **stop −3.67%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.43 (high win-rate)
- Gaps overnight (n=154) : méd. 0.0% · baisse 43% (gap-down >1% 15% · >2% 7%)
- Excursion ouverture 5min (n=155) : bas méd −0.73% (p90 −2.22%) · haut méd +0.87% · range méd 2.05%
- Excursion ouverture 15min (n=155) : bas méd −0.91% (p90 −2.92%) · haut méd +0.91% · range méd 2.32%
- Excursion ouverture 30min (n=155) : bas méd −1.08% (p90 −2.94%) · haut méd +1.15% · range méd 2.66%
- Excursion ouverture 60min (n=155) : bas méd −1.16% (p90 −3.0%) · haut méd +1.49% · range méd 2.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 86700.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 79% (114/154) · gap 25% · délai 0.3min · rebond 57% (52/114) (MFE +1.31%)
   - −1.0% : fill 30min 53% · séance 69% (102/154) · gap 15% · délai 2.0min · rebond 58% (51/102) (MFE +1.26%)
   - −1.5% : fill 30min 42% · séance 56% (78/154) · gap 9% · délai 2.9min · rebond 63% (42/78) (MFE +1.51%)
   - −2.0% : fill 30min 28% · séance 44% (63/154) · gap 7% · délai 8.1min · rebond 68% (37/63) (MFE +1.56%)
   - −3.0% : fill 30min 13% · séance 31% (41/154) · gap 2% · délai 56.1min · rebond 60% (19/41) (MFE +1.4%)
   - −4.0% : fill 30min 5% · séance 18% (27/154) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 4% · séance 13% (20/154) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.61%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.41%) → stop au-delà de −1.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.48%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=543 jambes) : jambe baissière méd −1.08% (p90 −2.41%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 95% (45/46) · rebond 62% (24/45)
      · −2.0% : fill 72% (32/46) · rebond 65% (17/32)
      · −3.0% : fill 50% (21/46) · rebond 66% (10/21)
      · −4.0% : fill 32% (16/46) · rebond 70% (9/16)
      · −5.0% : fill 22% (12/46) · rebond 85% (8/12)
   - **flat** (43 séances) :
      · −1.0% : fill 69% (30/43) · rebond 51% (13/30)
      · −2.0% : fill 40% (19/43) · rebond 77% (13/19)
      · −3.0% : fill 32% (12/43) · rebond 61% (6/12)
      · −4.0% : fill 24% (9/43) · rebond 50% (4/9)
      · −5.0% : fill 18% (7/43) · rebond 84% (5/7)
   - **gap-up** (65 séances) :
      · −1.0% : fill 49% (27/65) · rebond 62% (14/27)
      · −2.0% : fill 26% (12/65) · rebond 63% (7/12)
      · −3.0% : fill 17% (8/65) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/65) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/65) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=155) : 45% en base · 73% si les 15 1res min sont vertes (58 cas) · 22% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=155) : COUDE à **45min** → P(séance verte=clôture>ouverture) 79% si début vert vs 15% si rouge (base 45% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **79%** · continue >prix actuel 51% ; creux résiduel méd -1.54% (q20 -3.12%) → **SL/trailing à −3.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.22% → **scale +1.29% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **15%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.57%** (au-delà de la MAE q10 -3.57%), cible rebond +1.27% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=155) : retour [-2.64% .. +2.96%] · haut q95 +3.65% · bas q05 -3.36%
   - 60min (n=155) : retour [-2.93% .. +4.16%] · haut q95 +5.17% · bas q05 -4.03%
   - 2h (n=155) : retour [-3.23% .. +4.38%] · haut q95 +5.43% · bas q05 -4.06%
   - 4h (n=155) : retour [-4.23% .. +5.22%] · haut q95 +6.28% · bas q05 -5.79%
   - 6h (n=155) : retour [-4.65% .. +4.33%] · haut q95 +7.06% · bas q05 -6.0%
   - session (n=155) : retour [-4.75% .. +4.89%] · haut q95 +7.06% · bas q05 -6.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.45%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 59.6  _(momentum haussier)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist 863.199  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 21.8%
- **ATR** : 4100.0 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.07  _(accumulation)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 82210.0 · MA50 83824.0 · MA200 105110.0  _(prix > MA20)_
- **Dist MA** : MA20 +2.8% · MA50 +0.8% · MA200 -19.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81145 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
