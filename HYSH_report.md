# 298040

**Generated** : 2026-07-17T21:53:54.610464+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2789000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩2789000.00 (+1.1% vs entrée) · entrée ₩2759500.00 · stop ₩2538740.00 · T1 ₩2846194.03 · R/R 0.39  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.107 _(réel 5 s)_ (GBM -0.114) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2742161.19–₩2776838.81 (mid ₩2759500.00)
- Spot actuel : ₩2789000.00 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : ₩2538740.00 (stop swing_plan-based (-5.76%))
- Targets : T1 ₩2846194.03 · R/R 0.39 | T2 ₩2932888.06 · R/R 0.79 | T3 ₩3019582.09 · R/R 1.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2538740.00


## Edge, scénarios & sizing

- EV/risk : -0.114 | EV/share : ₩-25193.076 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.119 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.5 | bear 75.9 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.054% → cible +3.142% / stop −8.0%, p_fill 90%, n_eff≈35.1) : P(cible|rempli) **40%** · **EV/risk -0.107** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −2.329% → cible +7.025% / stop −3.512%, p_fill 88%, n_eff≈34.0) : P(cible|rempli) **30%** · **EV/risk -0.136** (×p_fill ; si rempli -0.54% du capital)
  - **deep** (entrée dip −3.602% → cible +9.935% / stop −4.967%, p_fill 84%, n_eff≈31.3) : P(cible|rempli) **29%** · **EV/risk -0.145** (×p_fill ; si rempli -0.86% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→62% · +2.0%→51% · +3.0%→36% · +5.0%→21% · +8.0%→6%
- Range intraday médian 6.78% (p90 9.64%) · excursion haute méd. +2.1% / basse méd. −3.63%
- Profil de vol intra : ouverture 4.117% vs midi 1.056% vs clôture 1.137% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 76% · range 22% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.069)_ ; drift intra méd. -1.59% ; recovery-V 32%
- **σ réalisé intraday** 5.169% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 69% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 2771875.0 (VA 2730175.0–2785775.0 ; dernier close 2762000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 92% · **stop −5.35%** sous le fill (sous le bruit) · cible +2.4% · R/R 0.45 (high win-rate)
- Gaps overnight (n=133) : méd. 0.6% · baisse 38% (gap-down >1% 24% · >2% 16%)
- Excursion ouverture 5min (n=134) : bas méd −1.28% (p90 −3.42%) · haut méd +0.81% · range méd 2.67%
- Excursion ouverture 15min (n=134) : bas méd −1.93% (p90 −4.79%) · haut méd +1.07% · range méd 3.5%
- Excursion ouverture 30min (n=134) : bas méd −2.4% (p90 −4.92%) · haut méd +1.11% · range méd 4.05%
- Excursion ouverture 60min (n=134) : bas méd −2.54% (p90 −5.32%) · haut méd +1.35% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2762000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 70% (91/133) · gap 32% · délai 0.1min · rebond 59% (56/91) (MFE +1.31%)
   - −1.0% : fill 30min 57% · séance 67% (83/133) · gap 24% · délai 0.6min · rebond 59% (51/83) (MFE +1.52%)
   - −1.5% : fill 30min 48% · séance 59% (74/133) · gap 20% · délai 1.2min · rebond 52% (45/74) (MFE +1.3%)
   - −2.0% : fill 30min 42% · séance 55% (65/133) · gap 16% · délai 2.6min · rebond 51% (35/65) (MFE +1.1%)
   - −3.0% : fill 30min 31% · séance 46% (53/133) · gap 8% · délai 5.3min · rebond 56% (30/53) (MFE +1.27%)
   - −4.0% : fill 30min 20% · séance 41% (45/133) · gap 5% · délai 33.4min · rebond 74% (34/45) (MFE +1.8%)
   - −5.0% : fill 30min 18% · séance 34% (34/133) · gap 4% · délai 28.4min · rebond 92% (29/34) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.36%) → stop au-delà de −2.36% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −3.65%) → stop au-delà de −2.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −3.75%) → stop au-delà de −2.1% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=700 jambes) : jambe baissière méd −1.43% (p90 −3.48%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 100% (46/46) · rebond 61% (29/46)
      · −2.0% : fill 86% (38/46) · rebond 54% (21/38)
      · −3.0% : fill 82% (36/46) · rebond 55% (20/36)
      · −4.0% : fill 76% (31/46) · rebond 77% (23/31)
      · −5.0% : fill 68% (26/46) · rebond 89% (21/26)
   - **flat** (15 séances) :
      · −1.0% : fill 82% (10/15) · rebond 57% (7/10)
      · −2.0% : fill 72% (7/15) · rebond 73% (5/7)
      · −3.0% : fill 43% (4/15) · rebond 100% (4/4)
      · −4.0% : fill 43% (4/15) · rebond 63% (3/4)
      · −5.0% : fill 31% (2/15) · rebond 100% (2/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 43% (27/72) · rebond 56% (15/27)
      · −2.0% : fill 32% (20/72) · rebond 35% (9/20)
      · −3.0% : fill 24% (13/72) · rebond 43% (6/13)
      · −4.0% : fill 18% (10/72) · rebond 71% (8/10)
      · −5.0% : fill 12% (6/72) · rebond 100% (6/6)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 40% en base · 66% si les 15 1res min sont vertes (54 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=134) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 81% si début vert vs 12% si rouge (base 40% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **81%** · continue >prix actuel 52% ; creux résiduel méd -1.5% (q20 -3.91%) → **SL/trailing à −3.91%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.9% → **scale +1.55% / runner +2.9%**, sortie à la clôture
  - **si ROUGE au coude** (n=73) : edge inversé — récupère vert seulement **12%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.08%** (au-delà de la MAE q10 -6.08%), cible rebond +1.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-4.52% .. +4.3%] · haut q95 +5.89% · bas q05 -5.24%
   - 60min (n=134) : retour [-5.35% .. +4.94%] · haut q95 +6.71% · bas q05 -5.98%
   - 2h (n=134) : retour [-7.38% .. +4.55%] · haut q95 +7.27% · bas q05 -8.22%
   - 4h (n=134) : retour [-7.94% .. +5.38%] · haut q95 +8.17% · bas q05 -9.68%
   - 6h (n=134) : retour [-7.57% .. +5.24%] · haut q95 +8.49% · bas q05 -9.51%
   - session (n=134) : retour [-6.71% .. +5.44%] · haut q95 +8.49% · bas q05 -9.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 5.2% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.85%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 43.5  _(momentum baissier)_
- **ADX** : 14.4  _(pas de tendance nette)_
- **MACD** : hist -39324.209  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 49.0%
- **ATR** : 288571.43 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.228  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 41.1  _(transition)_
- **MA** : MA20 3181400.0 · MA50 3550520.0 · MA200 2589134.01  _(prix < MA20)_
- **Dist MA** : MA20 -12.3% · MA50 -21.4% · MA200 +7.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82881 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
