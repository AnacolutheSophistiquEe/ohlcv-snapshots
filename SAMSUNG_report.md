# 005930

**Generated** : 2026-08-06T21:50:23.976470+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩230250.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩230250.00 (+2.0% vs entrée) · entrée ₩225749.65 · stop ₩201406.79 · T1 ₩261711.37 · R/R 1.48  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.41 _(réel 5 s)_ (GBM 0.187) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩221249.30–₩230250.00 (mid ₩225749.65)
- Spot actuel : ₩230250.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩201406.79 (stop swing_plan-based (-12.53%))
- Targets : T1 ₩261711.37 · R/R 1.48 | T2 ₩287183.29 · R/R 2.52 | T3 ₩294876.71 · R/R 2.84
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩201406.79


## Edge, scénarios & sizing

- EV/risk : 0.187 | EV/share : ₩4558.300 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 2 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 39.5 | bear 49.8 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.888% → cible +5.166% / stop −3.2%, p_fill 88%, n_eff≈34.1) : P(cible|rempli) **10%** · **EV/risk -0.464** (×p_fill ; si rempli -1.69% du capital)
  - **swing** (entrée dip −1.958% → cible +15.93% / stop −10.783%, p_fill 80%, n_eff≈30.5) : P(cible|rempli) **8%** · **EV/risk -0.410** (×p_fill ; si rempli -5.51% du capital)
  - **deep** (entrée dip −2.942% → cible +28.501% / stop −16.338%, p_fill 76%, n_eff≈29.2) : P(cible|rempli) **2%** · **EV/risk -0.415** (×p_fill ; si rempli -8.95% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→66% · +2.0%→48% · +3.0%→34% · +5.0%→21% · +8.0%→5%
- Range intraday médian 5.97% (p90 9.84%) · excursion haute méd. +1.93% / basse méd. −3.0%
- Profil de vol intra : ouverture 3.023% vs midi 1.333% vs clôture 1.516% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 70% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.082)_ ; drift intra méd. -1.529% ; recovery-V 19%
- **σ réalisé intraday** 4.706% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 39% / bas 78% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 248625.0 (VA 246875.0–249625.0 ; dernier close 247000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 61% · **stop −6.83%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.2 (high win-rate)
- Gaps overnight (n=147) : méd. 0.47% · baisse 43% (gap-down >1% 34% · >2% 24%)
- Excursion ouverture 5min (n=148) : bas méd −0.68% (p90 −1.64%) · haut méd +0.64% · range méd 1.55%
- Excursion ouverture 15min (n=148) : bas méd −1.1% (p90 −2.77%) · haut méd +1.04% · range méd 2.23%
- Excursion ouverture 30min (n=148) : bas méd −1.38% (p90 −3.51%) · haut méd +1.1% · range méd 2.9%
- Excursion ouverture 60min (n=148) : bas méd −1.74% (p90 −3.65%) · haut méd +1.18% · range méd 3.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 247000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 67% (92/147) · gap 37% · délai 0.0min · rebond 53% (50/92) (MFE +1.15%)
   - −1.0% : fill 30min 50% · séance 65% (86/147) · gap 34% · délai 0.0min · rebond 59% (49/86) (MFE +1.39%)
   - −1.5% : fill 30min 44% · séance 59% (76/147) · gap 26% · délai 0.3min · rebond 57% (45/76) (MFE +1.65%)
   - −2.0% : fill 30min 39% · séance 52% (67/147) · gap 24% · délai 0.5min · rebond 54% (38/67) (MFE +1.48%)
   - −3.0% : fill 30min 31% · séance 48% (58/147) · gap 20% · délai 2.7min · rebond 57% (37/58) (MFE +1.86%)
   - −4.0% : fill 30min 24% · séance 40% (46/147) · gap 15% · délai 23.2min · rebond 61% (31/46) (MFE +1.53%)
   - −5.0% : fill 30min 15% · séance 31% (35/147) · gap 11% · délai 59.0min · rebond 61% (23/35) (MFE +1.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.38%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −3.15%) → stop au-delà de −1.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −4.24%) → stop au-delà de −1.81% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=684 jambes) : jambe baissière méd −1.3% (p90 −3.16%) · ~13.0 jambes/séance
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
   - **gap-up** (72 séances) :
      · −1.0% : fill 40% (20/72) · rebond 81% (15/20)
      · −2.0% : fill 24% (12/72) · rebond 83% (10/12)
      · −3.0% : fill 18% (8/72) · rebond 76% (6/8)
      · −4.0% : fill 14% (6/72) · rebond 94% (5/6)
      · −5.0% : fill 5% (3/72) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 39% en base · 65% si les 15 1res min sont vertes (71 cas) · 17% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=148) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 83% si début vert vs 6% si rouge (base 39% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 75min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **83%** · continue >prix actuel 53% ; creux résiduel méd -1.67% (q20 -4.25%) → **SL/trailing à −4.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +3.48% → **scale +1.72% / runner +3.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=70) : edge inversé — récupère vert seulement **6%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.14%** (au-delà de la MAE q10 -7.14%), cible rebond +1.33% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-2.82% .. +2.86%] · haut q95 +3.7% · bas q05 -3.88%
   - 60min (n=148) : retour [-3.23% .. +4.81%] · haut q95 +5.61% · bas q05 -5.31%
   - 2h (n=148) : retour [-4.94% .. +4.53%] · haut q95 +6.29% · bas q05 -6.54%
   - 4h (n=148) : retour [-6.56% .. +5.51%] · haut q95 +6.83% · bas q05 -8.0%
   - 6h (n=148) : retour [-7.22% .. +5.4%] · haut q95 +7.12% · bas q05 -8.27%
   - session (n=148) : retour [-7.51% .. +5.46%] · haut q95 +7.12% · bas q05 -9.17%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.1% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.93%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.1  _(momentum baissier)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist 796.406  _(bullish_recent)_
- **BB** : %B 0.27 · largeur 34.7%
- **ATR** : 24342.86 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.237  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 51.8  _(transition)_
- **MA** : MA20 250287.5 · MA50 295124.16 · MA200 195634.41  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -22.0% · MA200 +17.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82195 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
