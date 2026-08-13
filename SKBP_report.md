# 326030

**Generated** : 2026-08-13T00:20:14.798815+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩88200.00  

> 🟡 **WAIT-FOR-DIP** — spot +4.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩88200.00 (+4.3% vs entrée) · entrée ₩84588.33 · stop ₩80245.48 · T1 ₩87300.81 · R/R 0.62  
> ↳ P(T1 av. stop) 67 % _(réel 5 s)_ · EV/risk 0.043 _(réel 5 s)_ (GBM -0.057) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩84045.84–₩85130.83 (mid ₩84588.33)
- Spot actuel : ₩88200.00 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : ₩80245.48 (stop swing_plan-based (-9.02%))
- Targets : T1 ₩87300.81 · R/R 0.62 | T2 ₩90013.28 · R/R 1.25 | T3 ₩92725.75 · R/R 1.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩80245.48


## Edge, scénarios & sizing

- EV/risk : -0.057 | EV/share : ₩-248.213 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 29 % | T3 12 %
- Kelly (position) : f* 0.024 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 61.9 | bear 15.0 | side 23.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.863% → cible +1.434% / stop −1.505%, p_fill 46%, n_eff≈22.6) : P(cible|rempli) **67%** · **EV/risk +0.139** (×p_fill ; si rempli +0.45% du capital)
  - **swing** (entrée dip −4.096% → cible +3.207% / stop −5.134%, p_fill 33%, n_eff≈17.1) : P(cible|rempli) **67%** · **EV/risk +0.043** (×p_fill ; si rempli +0.66% du capital)
  - **deep** (entrée dip −6.324% → cible +4.535% / stop −7.885%, p_fill 47%, n_eff≈17.5) : P(cible|rempli) **87%** · **EV/risk +0.168** (×p_fill ; si rempli +2.79% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→70% · +2.0%→51% · +3.0%→36% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.47% (p90 7.69%) · excursion haute méd. +2.1% / basse méd. −2.0%
- Profil de vol intra : ouverture 2.96% vs midi 0.907% vs clôture 0.892% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑1%/↓1% ; spike-down 56% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.096)_ ; drift intra méd. 0.459% ; recovery-V 40%
- **σ réalisé intraday** 3.486% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 52% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 90652.5 (VA 90442.5–91597.5 ; dernier close 91000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 45% · rebond 71% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.6% · R/R 0.42 (high win-rate)
- Gaps overnight (n=151) : méd. 0.0% · baisse 44% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=152) : bas méd −0.7% (p90 −2.22%) · haut méd +0.89% · range méd 2.06%
- Excursion ouverture 15min (n=152) : bas méd −0.87% (p90 −2.93%) · haut méd +1.0% · range méd 2.41%
- Excursion ouverture 30min (n=152) : bas méd −1.04% (p90 −2.94%) · haut méd +1.35% · range méd 2.77%
- Excursion ouverture 60min (n=152) : bas méd −1.16% (p90 −3.04%) · haut méd +1.65% · range méd 3.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 91000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 78% (111/151) · gap 26% · délai 0.3min · rebond 58% (51/111) (MFE +1.52%)
   - −1.0% : fill 30min 52% · séance 68% (99/151) · gap 16% · délai 1.7min · rebond 61% (50/99) (MFE +1.42%)
   - −1.5% : fill 30min 40% · séance 53% (75/151) · gap 9% · délai 1.8min · rebond 66% (41/75) (MFE +1.52%)
   - −2.0% : fill 30min 28% · séance 45% (62/151) · gap 7% · délai 10.2min · rebond 71% (37/62) (MFE +1.6%)
   - −3.0% : fill 30min 11% · séance 31% (40/151) · gap 3% · délai 79.9min · rebond 58% (18/40) (MFE +1.39%)
   - −4.0% : fill 30min 6% · séance 20% (27/151) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 4% · séance 14% (20/151) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.28% (p90 −2.65%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.46% (p90 −1.41%) → stop au-delà de −1.16% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.48%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=530 jambes) : jambe baissière méd −1.11% (p90 −2.43%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 66% (24/44)
      · −2.0% : fill 70% (31/45) · rebond 70% (17/31)
      · −3.0% : fill 46% (20/45) · rebond 61% (9/20)
      · −4.0% : fill 35% (16/45) · rebond 70% (9/16)
      · −5.0% : fill 23% (12/45) · rebond 85% (8/12)
   - **flat** (42 séances) :
      · −1.0% : fill 67% (29/42) · rebond 56% (13/29)
      · −2.0% : fill 42% (19/42) · rebond 77% (13/19)
      · −3.0% : fill 34% (12/42) · rebond 61% (6/12)
      · −4.0% : fill 26% (9/42) · rebond 50% (4/9)
      · −5.0% : fill 20% (7/42) · rebond 84% (5/7)
   - **gap-up** (64 séances) :
      · −1.0% : fill 47% (26/64) · rebond 58% (13/26)
      · −2.0% : fill 28% (12/64) · rebond 63% (7/12)
      · −3.0% : fill 18% (8/64) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/64) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/64) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 47% en base · 76% si les 15 1res min sont vertes (57 cas) · 24% si rouges (95 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=152) : COUDE à **45min** → P(séance verte=clôture>ouverture) 79% si début vert vs 16% si rouge (base 47% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **79%** · continue >prix actuel 51% ; creux résiduel méd -1.54% (q20 -3.12%) → **SL/trailing à −3.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.22% → **scale +1.29% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **16%** (continue à baisser 53%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.62%** (au-delà de la MAE q10 -3.62%), cible rebond +1.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-2.67% .. +3.25%] · haut q95 +3.77% · bas q05 -3.57%
   - 60min (n=152) : retour [-3.1% .. +4.2%] · haut q95 +5.36% · bas q05 -4.04%
   - 2h (n=152) : retour [-3.23% .. +4.55%] · haut q95 +5.54% · bas q05 -4.2%
   - 4h (n=152) : retour [-4.29% .. +5.58%] · haut q95 +6.42% · bas q05 -5.86%
   - 6h (n=152) : retour [-4.78% .. +4.36%] · haut q95 +7.24% · bas q05 -6.12%
   - session (n=152) : retour [-4.87% .. +5.06%] · haut q95 +7.24% · bas q05 -6.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.44%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 65.8  _(momentum haussier)_
- **ADX** : 19.6  _(pas de tendance nette)_
- **MACD** : hist 1580.698  _(pas de croisement recent)_
- **BB** : %B 0.93 · largeur 21.0%
- **ATR** : 4342.86 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.101  _(accumulation)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 42.7  _(transition)_
- **MA** : MA20 80960.0 · MA50 83976.0 · MA200 105421.0  _(prix > MA20)_
- **Dist MA** : MA20 +8.9% · MA50 +5.0% · MA200 -16.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81210 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
