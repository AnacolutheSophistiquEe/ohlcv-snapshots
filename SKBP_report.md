# 326030

**Generated** : 2026-08-14T00:19:52.463037+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩87600.00  

> 🟡 **WAIT-FOR-DIP** — spot +3.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩87600.00 (+3.9% vs entrée) · entrée ₩84318.33 · stop ₩80082.62 · T1 ₩86870.54 · R/R 0.6  
> ↳ P(T1 av. stop) 74 % _(réel 5 s)_ · EV/risk 0.077 _(réel 5 s)_ (GBM -0.054) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩83807.89–₩84828.77 (mid ₩84318.33)
- Spot actuel : ₩87600.00 (+3.9% au-dessus de la zone — repli à attendre)
- Stop : ₩80082.62 (stop swing_plan-based (-8.58%))
- Targets : T1 ₩86870.54 · R/R 0.6 | T2 ₩89422.74 · R/R 1.21 | T3 ₩91974.95 · R/R 1.81
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩80082.62


## Edge, scénarios & sizing

- EV/risk : -0.054 | EV/share : ₩-230.275 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 31 % | T3 16 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 62.5 | bear 30.3 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.706% → cible +1.354% / stop −1.5%, p_fill 47%, n_eff≈23.2) : P(cible|rempli) **69%** · **EV/risk +0.135** (×p_fill ; si rempli +0.43% du capital)
  - **swing** (entrée dip −3.745% → cible +3.027% / stop −5.023%, p_fill 36%, n_eff≈18.9) : P(cible|rempli) **74%** · **EV/risk +0.077** (×p_fill ; si rempli +1.08% du capital)
  - **deep** (entrée dip −5.787% → cible +4.281% / stop −7.699%, p_fill 53%, n_eff≈19.6) : P(cible|rempli) **84%** · **EV/risk +0.146** (×p_fill ; si rempli +2.15% du capital)
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

- **RSI** : 63.2  _(momentum haussier)_
- **ADX** : 20.0  _(pas de tendance nette)_
- **MACD** : hist 1420.684  _(pas de croisement recent)_
- **BB** : %B 0.85 · largeur 21.8%
- **ATR** : 4235.71 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.081  _(accumulation)_
- **Vol ratio** : 1.17  _(volume normal)_
- **Choppiness** : 41.8  _(transition)_
- **MA** : MA20 81430.0 · MA50 83960.0 · MA200 105323.5  _(prix > MA20)_
- **Dist MA** : MA20 +7.6% · MA50 +4.3% · MA200 -16.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81203 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
