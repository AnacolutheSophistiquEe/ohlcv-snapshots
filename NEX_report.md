# NEX

**Generated** : 2026-08-07T21:43:13.252725+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €139.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €139.60 (+6.3% vs entrée) · entrée €131.33 · stop €126.24 · T1 €134.70 · R/R 0.66  
> ↳ P(T1 av. stop) 69 % · EV/risk 0.097 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.65–€132.00 (mid €131.33)
- Spot actuel : €139.60 (+6.3% au-dessus de la zone — repli à attendre)
- Stop : €126.24 (stop swing_plan-based (-9.57%))
- Targets : T1 €134.70 · R/R 0.66 | T2 €138.08 · R/R 1.33 | T3 €141.46 · R/R 1.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.24


## Edge, scénarios & sizing

- EV/risk : -0.036 | EV/share : €-0.185 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 26 % | T3 11 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.8 | bear 48.2 | side 28.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 419.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.696% → cible +1.15% / stop −8.0%, p_fill 36%, n_eff≈15.0) : P(cible|rempli) **52%** · **EV/risk +0.013** (×p_fill ; si rempli +0.28% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=7, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→68% · +1.0%→54% · +2.0%→29% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.11% (p90 5.26%) · excursion haute méd. +1.07% / basse méd. −1.4%
- Profil de vol intra : ouverture 1.811% vs midi 0.561% vs clôture 0.778% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; mean-reverting — autocorr -0.034)_ ; drift intra méd. -0.616% ; recovery-V 16%
- **σ réalisé intraday** 2.302% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 71% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 141.28 (VA 140.64–141.76 ; dernier close 141.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 24% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=148) : méd. 0.17% · baisse 36% (gap-down >1% 9% · >2% 2%)
- Excursion ouverture 5min (n=149) : bas méd −0.46% (p90 −2.13%) · haut méd +0.33% · range méd 1.12%
- Excursion ouverture 15min (n=149) : bas méd −0.59% (p90 −2.23%) · haut méd +0.44% · range méd 1.4%
- Excursion ouverture 30min (n=149) : bas méd −0.6% (p90 −2.37%) · haut méd +0.55% · range méd 1.43%
- Excursion ouverture 60min (n=149) : bas méd −0.84% (p90 −2.59%) · haut méd +0.6% · range méd 1.61%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 141.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 70% (105/148) · gap 22% · délai 0.5min · rebond 45% (51/105) (MFE +0.86%)
   - −1.0% : fill 30min 39% · séance 63% (88/148) · gap 9% · délai 9.4min · rebond 48% (42/88) (MFE +0.98%)
   - −1.5% : fill 30min 24% · séance 50% (66/148) · gap 3% · délai 29.5min · rebond 50% (32/66) (MFE +1.01%)
   - −2.0% : fill 30min 16% · séance 34% (49/148) · gap 2% · délai 56.4min · rebond 49% (26/49) (MFE +0.99%)
   - −3.0% : fill 30min 4% · séance 24% (31/148) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 8% (11/148) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/148) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.14% (p90 −1.53%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.14% (p90 −1.79%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.92%) → stop au-delà de −0.55% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=317 jambes) : jambe baissière méd −1.05% (p90 −2.46%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (36 séances) :
      · −1.0% : fill 70% (24/36) · rebond 49% (13/24)
      · −2.0% : fill 40% (12/36) · rebond 51% (6/12)
      · −3.0% : fill 30% (8/36) · rebond 46% (3/8)
      · −4.0% : fill 10% (2/36) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (68 séances) :
      · −1.0% : fill 49% (28/68) · rebond 51% (14/28)
      · −2.0% : fill 25% (12/68) · rebond 53% (7/12)
      · −3.0% : fill 16% (7/68) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/68) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/68) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 44% en base · 64% si les 15 1res min sont vertes (80 cas) · 20% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=149) : COUDE à **29min** → P(séance verte=clôture>ouverture) 71% si début vert vs 20% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 306min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **71%** · continue >prix actuel 47% ; creux résiduel méd -1.05% (q20 -2.01%) → **SL/trailing à −2.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.64% → **scale +0.97% / runner +1.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **20%** (continue à baisser 56%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.26%** (au-delà de la MAE q10 -3.26%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-2.05% .. +2.14%] · haut q95 +2.51% · bas q05 -2.72%
   - 60min (n=149) : retour [-2.88% .. +2.08%] · haut q95 +2.69% · bas q05 -3.25%
   - 2h (n=149) : retour [-3.63% .. +2.28%] · haut q95 +2.93% · bas q05 -3.8%
   - 4h (n=149) : retour [-3.41% .. +2.35%] · haut q95 +2.94% · bas q05 -4.02%
   - 6h (n=149) : retour [-3.82% .. +3.16%] · haut q95 +3.55% · bas q05 -4.19%
   - session (n=149) : retour [-3.61% .. +2.83%] · haut q95 +3.87% · bas q05 -4.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.96%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.0  _(momentum haussier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist 1.61  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 11.3%
- **ATR** : 5.09 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.026  _(neutre)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 50.3  _(transition)_
- **MA** : MA20 133.6 · MA50 142.36 · MA200 131.99  _(prix > MA20)_
- **Dist MA** : MA20 +4.5% · MA50 -1.9% · MA200 +5.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90906 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
