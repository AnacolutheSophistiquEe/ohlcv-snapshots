# 005930

**Generated** : 2026-08-05T21:49:45.262875+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩246000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩246000.00 (+0.8% vs entrée) · entrée ₩244131.31 · stop ₩235341.28 · T1 ₩261711.37 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % _(réel 5 s)_ · EV/risk -0.362 _(réel 5 s)_ (GBM -0.072) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.6% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩242262.62–₩246000.00 (mid ₩244131.31)
- Spot actuel : ₩246000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩235341.28 (stop swing_plan-based (-13.48%))
- Targets : T1 ₩261711.37 · R/R 2.0 | T2 ₩269625.64 · R/R 2.9 | T3 ₩277539.91 · R/R 3.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩235341.28


## Edge, scénarios & sizing

- EV/risk : -0.072 | EV/share : ₩-635.623 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.054 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 35.8 | bear 57.4 | side 6.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.757% → cible +7.201% / stop −3.601%, p_fill 89%, n_eff≈34.7) : P(cible|rempli) **6%** · **EV/risk -0.362** (×p_fill ; si rempli -1.47% du capital)
  - **swing** (entrée dip −1.682% → cible +24.931% / stop −12.0%, p_fill 82%, n_eff≈32.1) : P(cible|rempli) **0%** · **EV/risk -0.416** (×p_fill ; si rempli -6.08% du capital)
  - **deep** (entrée dip −2.455% → cible +14.425% / stop −15.618%, p_fill 77%, n_eff≈30.8) : P(cible|rempli) **16%** · **EV/risk -0.336** (×p_fill ; si rempli -6.81% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→66% · +2.0%→48% · +3.0%→34% · +5.0%→21% · +8.0%→5%
- Range intraday médian 5.86% (p90 9.84%) · excursion haute méd. +1.93% / basse méd. −2.85%
- Profil de vol intra : ouverture 2.971% vs midi 1.302% vs clôture 1.504% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 69% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.079)_ ; drift intra méd. -1.441% ; recovery-V 21%
- **σ réalisé intraday** 4.746% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 76% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 240562.5 (VA 238637.5–243037.5 ; dernier close 239000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 61% · **stop −6.83%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.2 (high win-rate)
- Gaps overnight (n=145) : méd. 0.22% · baisse 45% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=146) : bas méd −0.65% (p90 −1.61%) · haut méd +0.69% · range méd 1.55%
- Excursion ouverture 15min (n=146) : bas méd −1.01% (p90 −2.78%) · haut méd +1.05% · range méd 2.23%
- Excursion ouverture 30min (n=146) : bas méd −1.24% (p90 −3.23%) · haut méd +1.14% · range méd 2.91%
- Excursion ouverture 60min (n=146) : bas méd −1.62% (p90 −3.59%) · haut méd +1.35% · range méd 3.11%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 239000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 68% (91/145) · gap 38% · délai 0.0min · rebond 52% (49/91) (MFE +1.2%)
   - −1.0% : fill 30min 50% · séance 65% (85/145) · gap 36% · délai 0.0min · rebond 57% (48/85) (MFE +1.31%)
   - −1.5% : fill 30min 43% · séance 59% (75/145) · gap 27% · délai 0.3min · rebond 56% (44/75) (MFE +1.45%)
   - −2.0% : fill 30min 40% · séance 52% (66/145) · gap 25% · délai 0.2min · rebond 53% (37/66) (MFE +1.33%)
   - −3.0% : fill 30min 32% · séance 47% (57/145) · gap 21% · délai 1.7min · rebond 56% (36/57) (MFE +1.75%)
   - −4.0% : fill 30min 25% · séance 39% (45/145) · gap 16% · délai 15.7min · rebond 59% (30/45) (MFE +1.46%)
   - −5.0% : fill 30min 15% · séance 33% (35/145) · gap 11% · délai 59.0min · rebond 61% (23/35) (MFE +1.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.38%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −3.15%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −4.24%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=668 jambes) : jambe baissière méd −1.32% (p90 −3.16%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (62 séances) :
      · −1.0% : fill 98% (59/62) · rebond 46% (30/59)
      · −2.0% : fill 90% (51/62) · rebond 42% (25/51)
      · −3.0% : fill 87% (46/62) · rebond 50% (28/46)
      · −4.0% : fill 77% (38/62) · rebond 51% (24/38)
      · −5.0% : fill 67% (30/62) · rebond 55% (18/30)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (70 séances) :
      · −1.0% : fill 39% (19/70) · rebond 79% (14/19)
      · −2.0% : fill 22% (11/70) · rebond 80% (9/11)
      · −3.0% : fill 15% (7/70) · rebond 70% (5/7)
      · −4.0% : fill 11% (5/70) · rebond 92% (4/5)
      · −5.0% : fill 6% (3/70) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 40% en base · 65% si les 15 1res min sont vertes (71 cas) · 19% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=146) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 6% si rouge (base 40% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **83%** · continue >prix actuel 53% ; creux résiduel méd -1.67% (q20 -4.25%) → **SL/trailing à −4.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.48% → **scale +1.72% / runner +3.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=68) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.17%** (au-delà de la MAE q10 -7.17%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-2.77% .. +2.89%] · haut q95 +3.71% · bas q05 -3.68%
   - 60min (n=146) : retour [-3.13% .. +4.86%] · haut q95 +5.73% · bas q05 -5.08%
   - 2h (n=146) : retour [-5.04% .. +4.63%] · haut q95 +6.31% · bas q05 -5.72%
   - 4h (n=146) : retour [-6.61% .. +5.62%] · haut q95 +6.83% · bas q05 -8.11%
   - 6h (n=146) : retour [-7.35% .. +5.55%] · haut q95 +7.26% · bas q05 -8.51%
   - session (n=146) : retour [-7.56% .. +5.63%] · haut q95 +7.26% · bas q05 -9.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.3  _(momentum baissier)_
- **ADX** : 26.7  _(tendance etablie)_
- **MACD** : hist 970.297  _(bullish_recent)_
- **BB** : %B 0.42 · largeur 34.9%
- **ATR** : 24985.71 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.243  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 252650.0 · MA50 296492.58 · MA200 194937.5  _(prix < MA20)_
- **Dist MA** : MA20 -2.6% · MA50 -17.0% · MA200 +26.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83160 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
