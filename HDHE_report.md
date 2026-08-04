# 267260

**Generated** : 2026-08-04T21:51:43.014908+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩715000.00  

> 🟡 **WAIT-FOR-DIP** — spot +3.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩715000.00 (+3.4% vs entrée) · entrée ₩691340.13 · stop ₩636032.92 · T1 ₩740654.86 · R/R 0.89  
> ↳ P(T1 av. stop) 15 % _(réel 5 s)_ · EV/risk 0.017 _(réel 5 s)_ (GBM -0.186) · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩685441.20–₩697239.06 (mid ₩691340.13)
- Spot actuel : ₩715000.00 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : ₩636032.92 (stop swing_plan-based (-18.41%))
- Targets : T1 ₩740654.86 · R/R 0.89 | T2 ₩760105.39 · R/R 1.24 | T3 ₩779555.92 · R/R 1.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩636032.92


## Edge, scénarios & sizing

- EV/risk : -0.186 | EV/share : ₩-10314.795 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.3 | bear 79.5 | side 13.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.304% → cible +7.133% / stop −8.0%, p_fill 74%, n_eff≈30.2) : P(cible|rempli) **15%** · **EV/risk +0.017** (×p_fill ; si rempli +0.19% du capital)
  - **swing** (entrée dip −7.284% → cible +26.468% / stop −12.0%, p_fill 55%, n_eff≈20.7) : P(cible|rempli) **0%** · **EV/risk -0.173** (×p_fill ; si rempli -3.81% du capital)
  - **deep** (entrée dip −11.256% → cible +13.45% / stop −16.885%, p_fill 33%, n_eff≈18.0) : P(cible|rempli) **29%** · **EV/risk -0.046** (×p_fill ; si rempli -2.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→46% · +3.0%→34% · +5.0%→12% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.58%) · excursion haute méd. +1.84% / basse méd. −3.88%
- Profil de vol intra : ouverture 4.349% vs midi 1.188% vs clôture 1.229% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -2.254% ; recovery-V 18%
- **σ réalisé intraday** 5.015% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 69% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 687225.0 (VA 676775.0–700525.0 ; dernier close 672000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 82% · **stop −5.38%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.38 (high win-rate)
- Gaps overnight (n=145) : méd. 0.74% · baisse 40% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=146) : bas méd −1.74% (p90 −4.32%) · haut méd +0.98% · range méd 2.88%
- Excursion ouverture 15min (n=146) : bas méd −1.98% (p90 −4.87%) · haut méd +1.06% · range méd 3.58%
- Excursion ouverture 30min (n=146) : bas méd −2.34% (p90 −5.18%) · haut méd +1.14% · range méd 3.87%
- Excursion ouverture 60min (n=146) : bas méd −2.95% (p90 −5.72%) · haut méd +1.35% · range méd 4.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 672000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (103/145) · gap 32% · délai 0.0min · rebond 53% (57/103) (MFE +1.16%)
   - −1.0% : fill 30min 56% · séance 70% (96/145) · gap 22% · délai 0.2min · rebond 57% (57/96) (MFE +1.3%)
   - −1.5% : fill 30min 49% · séance 64% (83/145) · gap 15% · délai 0.4min · rebond 66% (54/83) (MFE +1.28%)
   - −2.0% : fill 30min 44% · séance 59% (75/145) · gap 11% · délai 0.7min · rebond 69% (51/75) (MFE +1.61%)
   - −3.0% : fill 30min 35% · séance 51% (60/145) · gap 7% · délai 1.8min · rebond 78% (42/60) (MFE +1.98%)
   - −4.0% : fill 30min 24% · séance 42% (49/145) · gap 4% · délai 8.1min · rebond 74% (38/49) (MFE +2.29%)
   - −5.0% : fill 30min 16% · séance 36% (39/145) · gap 2% · délai 37.6min · rebond 82% (30/39) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −3.76%) → stop au-delà de −2.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.96% (p90 −4.01%) → stop au-delà de −2.95% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.24% (p90 −5.23%) → stop au-delà de −3.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=745 jambes) : jambe baissière méd −1.3% (p90 −3.61%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 98% (50/51) · rebond 52% (27/50)
      · −2.0% : fill 93% (43/51) · rebond 64% (26/43)
      · −3.0% : fill 84% (37/51) · rebond 76% (25/37)
      · −4.0% : fill 71% (32/51) · rebond 73% (25/32)
      · −5.0% : fill 63% (25/51) · rebond 80% (19/25)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (77 séances) :
      · −1.0% : fill 48% (32/77) · rebond 69% (23/32)
      · −2.0% : fill 33% (20/77) · rebond 74% (16/20)
      · −3.0% : fill 24% (12/77) · rebond 77% (9/12)
      · −4.0% : fill 19% (10/77) · rebond 82% (8/10)
      · −5.0% : fill 14% (7/77) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 32% en base · 50% si les 15 1res min sont vertes (66 cas) · 22% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=146) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 68% si début vert vs 9% si rouge (base 32% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **68%** · continue >prix actuel 39% ; creux résiduel méd -1.99% (q20 -4.55%) → **SL/trailing à −4.55%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +2.75% → **scale +1.33% / runner +2.75%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **9%** (continue à baisser 56%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-5.55% .. +2.7%] · haut q95 +4.26% · bas q05 -5.79%
   - 60min (n=146) : retour [-5.73% .. +3.01%] · haut q95 +4.47% · bas q05 -6.88%
   - 2h (n=146) : retour [-7.04% .. +3.7%] · haut q95 +5.23% · bas q05 -7.92%
   - 4h (n=146) : retour [-6.95% .. +4.01%] · haut q95 +5.43% · bas q05 -8.86%
   - 6h (n=146) : retour [-8.29% .. +4.46%] · haut q95 +6.83% · bas q05 -9.45%
   - session (n=146) : retour [-7.66% .. +4.63%] · haut q95 +6.91% · bas q05 -9.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.48%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 43.7  _(momentum baissier)_
- **ADX** : 29.4  _(tendance etablie)_
- **MACD** : hist -2666.599  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 44.4%
- **ATR** : 71428.57 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.098  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 41.8  _(transition)_
- **MA** : MA20 766550.0 · MA50 919060.0 · MA200 922594.4  _(prix < MA20)_
- **Dist MA** : MA20 -6.7% · MA50 -22.2% · MA200 -22.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82521 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
