# 207940

**Generated** : 2026-07-17T00:20:37.472813+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1396000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)  
> ↳ spot ₩1396000.00 (+5.1% vs entrée) · entrée ₩1328075.00 · stop ₩1297269.58 · T1 ₩1389685.85 · R/R 2.0  
> ↳ P(T1 av. stop) 24 % · EV/risk -0.081 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1315752.83–₩1340397.17 (mid ₩1328075.00)
- Spot actuel : ₩1396000.00 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : ₩1297269.58 (stop swing_plan-based (-7.07%))
- Targets : T1 ₩1389685.85 · R/R 2.0 | T2 ₩1451296.69 · R/R 4.0 | T3 ₩1512907.54 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1297269.58


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : ₩-2494.514 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 9 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 47.8 | bear 17.4 | side 34.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.207% → cible +2.075% / stop −8.0%, p_fill 53%, n_eff≈21.0) : P(cible|rempli) **31%** · **EV/risk +0.006** (×p_fill ; si rempli +0.10% du capital)
  - **swing** (entrée dip −4.863% → cible +4.639% / stop −2.32%, p_fill 29%, n_eff≈9.6) : P(cible|rempli) **51%** · **EV/risk +0.165** (×p_fill ; si rempli +1.30% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=9, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→49% · +2.0%→35% · +3.0%→22% · +5.0%→4% · +8.0%→1%
- Range intraday médian 3.93% (p90 6.08%) · excursion haute méd. +0.9% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.282% vs midi 0.648% vs clôture 0.78% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (133 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 12% · trend ↑0%/↓4% ; spike-down 55% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.137 ; neutre — autocorr -0.012)_ ; drift intra méd. -0.451% ; recovery-V 27%
- **σ réalisé intraday** 3.134% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 60% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 1397525.0 (VA 1383875.0–1408025.0 ; dernier close 1381000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 17% · rebond 60% · **stop −1.96%** sous le fill (sous le bruit) · cible +1.72% · R/R 0.88 (high win-rate)
- Gaps overnight (n=132) : méd. 0.41% · baisse 29% (gap-down >1% 7% · >2% 5%)
- Excursion ouverture 5min (n=133) : bas méd −0.77% (p90 −2.4%) · haut méd +0.44% · range méd 1.52%
- Excursion ouverture 15min (n=133) : bas méd −1.07% (p90 −2.84%) · haut méd +0.58% · range méd 1.91%
- Excursion ouverture 30min (n=133) : bas méd −1.1% (p90 −3.05%) · haut méd +0.62% · range méd 2.41%
- Excursion ouverture 60min (n=133) : bas méd −1.26% (p90 −3.41%) · haut méd +0.69% · range méd 2.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1381000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 72% (87/132) · gap 17% · délai 1.1min · rebond 48% (36/87) (MFE +0.93%)
   - −1.0% : fill 30min 47% · séance 60% (70/132) · gap 7% · délai 2.0min · rebond 52% (29/70) (MFE +1.03%)
   - −1.5% : fill 30min 38% · séance 47% (53/132) · gap 6% · délai 3.4min · rebond 50% (23/53) (MFE +1.0%)
   - −2.0% : fill 30min 26% · séance 42% (47/132) · gap 5% · délai 8.9min · rebond 61% (24/47) (MFE +1.26%)
   - −3.0% : fill 30min 9% · séance 29% (30/132) · gap 2% · délai 116.1min · rebond 58% (16/30) (MFE +1.39%)
   - −4.0% : fill 30min 5% · séance 17% (16/132) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 9% (9/132) · gap 2% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.77% (p90 −2.01%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.17%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −2.53%) → stop au-delà de −1.94% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=307 jambes) : jambe baissière méd −1.1% (p90 −2.8%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (29 séances) :
      · −1.0% : fill 97% (28/29) · rebond 60% (13/28)
      · −2.0% : fill 84% (24/29) · rebond 61% (11/24)
      · −3.0% : fill 49% (13/29) · rebond 57% (7/13)
      · −4.0% : fill 28% (7/29) · rebond 58% (3/7)
      · −5.0% : fill 11% (4/29) · rebond 100% (4/4)
   - **flat** (41 séances) :
      · −1.0% : fill 69% (23/41) · rebond 31% (7/23)
      · −2.0% : fill 40% (10/41) · rebond 57% (5/10)
      · −3.0% : fill 30% (7/41) · rebond 97% (6/7)
      · −4.0% : fill 17% (4/41) · rebond 100% (4/4)
      · −5.0% : fill 8% (2/41) · rebond 89% (1/2)
   - **gap-up** (62 séances) :
      · −1.0% : fill 40% (19/62) · rebond 62% (9/19)
      · −2.0% : fill 25% (13/62) · rebond 63% (8/13)
      · −3.0% : fill 20% (10/62) · rebond 28% (3/10)
      · −4.0% : fill 12% (5/62) · rebond 33% (2/5)
      · −5.0% : fill 8% (3/62) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=133) : 36% en base · 60% si les 15 1res min sont vertes (44 cas) · 24% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=133) : COUDE à **31min** → P(séance verte=clôture>ouverture) 68% si début vert vs 20% si rouge (base 36% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=45) : tient le vert **68%** · continue >prix actuel 34% ; creux résiduel méd -1.47% (q20 -3.08%) → **SL/trailing à −3.08%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.4% / q75 +2.0% → **scale +1.4% / runner +2.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **20%** (continue à baisser 57%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.37%** (au-delà de la MAE q10 -3.37%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=133) : retour [-2.96% .. +3.03%] · haut q95 +3.26% · bas q05 -3.42%
   - 60min (n=133) : retour [-3.25% .. +2.58%] · haut q95 +3.4% · bas q05 -3.68%
   - 2h (n=133) : retour [-4.12% .. +3.42%] · haut q95 +4.26% · bas q05 -4.51%
   - 4h (n=133) : retour [-4.46% .. +3.82%] · haut q95 +4.82% · bas q05 -5.38%
   - 6h (n=133) : retour [-4.72% .. +4.07%] · haut q95 +4.82% · bas q05 -5.4%
   - session (n=133) : retour [-4.82% .. +3.67%] · haut q95 +4.82% · bas q05 -5.47%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.8% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.8  _(momentum haussier)_
- **ADX** : 11.3  _(pas de tendance nette)_
- **MACD** : hist 1443.324  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 12.3%
- **ATR** : 70500.0 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.078  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 69.9  _(marche en range (choppy))_
- **MA** : MA20 1378750.0 · MA50 1378300.0 · MA200 1616353.22  _(prix > MA20)_
- **Dist MA** : MA20 +1.3% · MA50 +1.3% · MA200 -13.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80860 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
