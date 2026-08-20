# SMR

**Generated** : 2026-08-20T00:27:08.166457+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.29  

> 🟡 **WAIT-FOR-DIP** — spot +0.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $9.29 (+0.9% vs entrée) · entrée $9.21 · stop $8.98 · T1 $9.66 · R/R 1.96  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk 0.03 _(réel 5 s)_ (GBM 0.11) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.47% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 134 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.15–$9.27 (mid $9.21)
- Spot actuel : $9.29 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $8.98 (stop swing_plan-based (-11.87%))
- Targets : T1 $9.66 · R/R 1.96 | T2 $9.89 · R/R 2.96 | T3 $10.11 · R/R 3.91
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $8.98


## Edge, scénarios & sizing

- EV/risk : 0.11 | EV/share : $0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.119 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 49.6 | bear 11.2 | side 39.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 158.0 (= 17 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.856% → cible +4.931% / stop −2.466%, p_fill 85%, n_eff≈35.4) : P(cible|rempli) **28%** · **EV/risk +0.030** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −1.873% → cible +20.377% / stop −10.188%, p_fill 80%, n_eff≈33.4) : P(cible|rempli) **12%** · **EV/risk +0.041** (×p_fill ; si rempli +0.53% du capital)
  - **deep** (entrée dip −2.897% → cible +10.255% / stop −11.135%, p_fill 74%, n_eff≈31.5) : P(cible|rempli) **49%** · **EV/risk -0.066** (×p_fill ; si rempli -0.98% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→81% · +2.0%→65% · +3.0%→60% · +5.0%→40% · +8.0%→14%
- Range intraday médian 7.6% (p90 12.48%) · excursion haute méd. +3.55% / basse méd. −3.15%
- Profil de vol intra : ouverture 4.88% vs midi 1.514% vs clôture 1.846% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 38%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.044)_ ; drift intra méd. 0.222% ; recovery-V 41%
- **σ réalisé intraday** 4.772% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 63% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 9.6216 (VA 9.3994–9.9363 ; dernier close 9.37)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 50% · rebond 77% · **stop −5.22%** sous le fill (sous le bruit) · cible +2.55% · R/R 0.49 (high win-rate)
- Gaps overnight (n=159) : méd. -0.57% · baisse 58% (gap-down >1% 36% · >2% 25%)
- Excursion ouverture 5min (n=160) : bas méd −1.08% (p90 −3.05%) · haut méd +1.29% · range méd 2.67%
- Excursion ouverture 15min (n=160) : bas méd −1.33% (p90 −3.83%) · haut méd +1.74% · range méd 3.71%
- Excursion ouverture 30min (n=160) : bas méd −1.79% (p90 −4.66%) · haut méd +2.23% · range méd 4.45%
- Excursion ouverture 60min (n=160) : bas méd −2.12% (p90 −5.72%) · haut méd +2.57% · range méd 5.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.37 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 72% · séance 81% (131/159) · gap 50% · délai 0.0min · rebond 67% (82/131) (MFE +1.87%)
   - −1.0% : fill 30min 67% · séance 78% (126/159) · gap 36% · délai 0.0min · rebond 70% (85/126) (MFE +2.14%)
   - −1.5% : fill 30min 63% · séance 74% (120/159) · gap 32% · délai 0.1min · rebond 75% (89/120) (MFE +2.24%)
   - −2.0% : fill 30min 56% · séance 66% (111/159) · gap 25% · délai 0.9min · rebond 69% (80/111) (MFE +2.44%)
   - −3.0% : fill 30min 43% · séance 56% (99/159) · gap 9% · délai 4.5min · rebond 75% (80/99) (MFE +2.05%)
   - −4.0% : fill 30min 34% · séance 50% (87/159) · gap 5% · délai 9.2min · rebond 77% (68/87) (MFE +2.55%)
   - −5.0% : fill 30min 24% · séance 40% (65/159) · gap 2% · délai 19.5min · rebond 75% (48/65) (MFE +2.38%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −2.67%) → stop au-delà de −1.8% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.71%) → stop au-delà de −2.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.12% (p90 −3.3%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1182 jambes) : jambe baissière méd −1.36% (p90 −3.23%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (87 séances) :
      · −1.0% : fill 100% (87/87) · rebond 69% (59/87)
      · −2.0% : fill 92% (82/87) · rebond 73% (62/82)
      · −3.0% : fill 81% (76/87) · rebond 77% (63/76)
      · −4.0% : fill 74% (69/87) · rebond 80% (57/69)
      · −5.0% : fill 59% (50/87) · rebond 78% (39/50)
   - **flat** (11 séances) :
      · −1.0% : fill 79% (8/11) · rebond 54% (5/8)
      · −2.0% : fill 68% (6/11) · rebond 18% (2/6)
      · −3.0% : fill 68% (6/11) · rebond 46% (3/6)
      · −4.0% : fill 68% (6/11) · rebond 56% (3/6)
      · −5.0% : fill 57% (5/11) · rebond 79% (4/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 46% (31/61) · rebond 78% (21/31)
      · −2.0% : fill 28% (23/61) · rebond 71% (16/23)
      · −3.0% : fill 19% (17/61) · rebond 80% (14/17)
      · −4.0% : fill 14% (12/61) · rebond 67% (8/12)
      · −5.0% : fill 10% (10/61) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 66% si les 15 1res min sont vertes (71 cas) · 32% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **2:01** → P(séance verte=clôture>ouverture) 88% si début vert vs 10% si rouge (base 48% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **88%** · continue >prix actuel 52% ; creux résiduel méd -1.79% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.88% / q75 +3.58% → **scale +1.88% / runner +3.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **10%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.57%** (au-delà de la MAE q10 -4.57%), cible rebond +1.4% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.38% .. +4.91%] · haut q95 +6.24% · bas q05 -5.9%
   - 60min (n=160) : retour [-5.62% .. +5.62%] · haut q95 +6.78% · bas q05 -6.83%
   - 2h (n=160) : retour [-6.57% .. +5.68%] · haut q95 +9.62% · bas q05 -8.01%
   - 4h (n=160) : retour [-7.29% .. +7.4%] · haut q95 +9.91% · bas q05 -9.33%
   - 6h (n=160) : retour [-7.38% .. +8.59%] · haut q95 +10.99% · bas q05 -9.57%
   - session (n=160) : retour [-7.34% .. +9.25%] · haut q95 +11.12% · bas q05 -9.96%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 5.0%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 56.2  _(momentum haussier)_
- **ADX** : 14.4  _(pas de tendance nette)_
- **MACD** : hist 0.035  _(pas de croisement recent)_
- **BB** : %B 0.6 · largeur 28.3%
- **ATR** : 0.67 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.004  _(neutre)_
- **Vol ratio** : 1.11  _(volume normal)_
- **Choppiness** : 61.6  _(transition)_
- **MA** : MA20 9.02 · MA50 9.32 · MA200 14.3  _(prix > MA20)_
- **Dist MA** : MA20 +3.0% · MA50 -0.3% · MA200 -35.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (102120 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
