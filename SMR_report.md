# SMR

**Generated** : 2026-08-07T00:30:03.166748+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $9.47  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $9.47 (+1.3% vs entrée) · entrée $9.35 · stop $9.14 · T1 $9.66 · R/R 1.48  
> ↳ P(T1 av. stop) 31 % _(réel 5 s)_ · EV/risk -0.066 _(réel 5 s)_ (GBM 0.106) · ¼-Kelly 0.028 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.18% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 159 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $9.28–$9.41 (mid $9.35)
- Spot actuel : $9.47 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : $9.14 (stop swing_plan-based (-12.26%))
- Targets : T1 $9.66 · R/R 1.48 | T2 $9.96 · R/R 2.9 | T3 $10.26 · R/R 4.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.14


## Edge, scénarios & sizing

- EV/risk : 0.106 | EV/share : $0.022 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 34 % | T3 34 %
- Kelly (position) : f* 0.114 | ¼-Kelly 0.028 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.1 | bear 16.7 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 284.0 (= 30 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.315% → cible +3.415% / stop −2.184%, p_fill 82%, n_eff≈32.4) : P(cible|rempli) **31%** · **EV/risk -0.066** (×p_fill ; si rempli -0.18% du capital)
  - **swing** (entrée dip −2.88% → cible +19.317% / stop −9.658%, p_fill 72%, n_eff≈28.5) : P(cible|rempli) **2%** · **EV/risk -0.226** (×p_fill ; si rempli -3.02% du capital)
  - **deep** (entrée dip −4.453% → cible +10.292% / stop −11.279%, p_fill 72%, n_eff≈30.0) : P(cible|rempli) **33%** · **EV/risk -0.239** (×p_fill ; si rempli -3.75% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→65% · +3.0%→60% · +5.0%→41% · +8.0%→19%
- Range intraday médian 7.83% (p90 12.61%) · excursion haute méd. +3.65% / basse méd. −3.15%
- Profil de vol intra : ouverture 5.165% vs midi 1.563% vs clôture 1.858% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. 0.188% ; recovery-V 41%
- **σ réalisé intraday** 4.894% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 66% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 9.0583 (VA 8.9148–9.0787 ; dernier close 9.025)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 51% · rebond 77% · **stop −5.95%** sous le fill (sous le bruit) · cible +2.56% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.46% · baisse 57% (gap-down >1% 42% · >2% 30%)
- Excursion ouverture 5min (n=160) : bas méd −1.12% (p90 −3.12%) · haut méd +1.11% · range méd 2.68%
- Excursion ouverture 15min (n=160) : bas méd −1.4% (p90 −3.53%) · haut méd +1.52% · range méd 3.58%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −4.57%) · haut méd +2.21% · range méd 4.42%
- Excursion ouverture 60min (n=160) : bas méd −2.13% (p90 −5.68%) · haut méd +2.85% · range méd 5.41%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.025 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 73% · séance 81% (131/159) · gap 49% · délai 0.0min · rebond 68% (82/131) (MFE +2.0%)
   - −1.0% : fill 30min 67% · séance 78% (126/159) · gap 42% · délai 0.0min · rebond 70% (85/126) (MFE +2.23%)
   - −1.5% : fill 30min 62% · séance 76% (120/159) · gap 38% · délai 0.0min · rebond 76% (90/120) (MFE +2.34%)
   - −2.0% : fill 30min 56% · séance 68% (112/159) · gap 30% · délai 0.1min · rebond 70% (82/112) (MFE +2.52%)
   - −3.0% : fill 30min 45% · séance 58% (99/159) · gap 11% · délai 2.1min · rebond 75% (80/99) (MFE +2.6%)
   - −4.0% : fill 30min 34% · séance 51% (84/159) · gap 6% · délai 11.3min · rebond 77% (65/84) (MFE +2.56%)
   - −5.0% : fill 30min 24% · séance 40% (63/159) · gap 3% · délai 19.6min · rebond 71% (46/63) (MFE +2.13%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −2.7%) → stop au-delà de −2.05% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.92%) → stop au-delà de −2.14% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.05% (p90 −3.21%) → stop au-delà de −2.38% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1177 jambes) : jambe baissière méd −1.39% (p90 −3.23%) · ~14.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 100% (84/84) · rebond 70% (57/84)
      · −2.0% : fill 94% (80/84) · rebond 75% (61/80)
      · −3.0% : fill 85% (75/84) · rebond 77% (62/75)
      · −4.0% : fill 75% (66/84) · rebond 81% (54/66)
      · −5.0% : fill 60% (48/84) · rebond 74% (37/48)
   - **flat** (13 séances) :
      · −1.0% : fill 80% (10/13) · rebond 53% (6/10)
      · −2.0% : fill 69% (8/13) · rebond 22% (4/8)
      · −3.0% : fill 66% (6/13) · rebond 46% (3/6)
      · −4.0% : fill 66% (6/13) · rebond 56% (3/6)
      · −5.0% : fill 56% (5/13) · rebond 79% (4/5)
   - **gap-up** (62 séances) :
      · −1.0% : fill 48% (32/62) · rebond 76% (22/32)
      · −2.0% : fill 33% (24/62) · rebond 71% (17/24)
      · −3.0% : fill 22% (18/62) · rebond 80% (15/18)
      · −4.0% : fill 16% (12/62) · rebond 67% (8/12)
      · −5.0% : fill 11% (10/62) · rebond 42% (5/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 60% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 68% si début vert vs 19% si rouge (base 47% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=84) : tient le vert **68%** · continue >prix actuel 46% ; creux résiduel méd -3.01% (q20 -5.04%) → **SL/trailing à −5.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.27% / q75 +4.64% → **scale +2.27% / runner +4.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **19%** (continue à baisser 54%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.71%** (au-delà de la MAE q10 -6.71%), cible rebond +2.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.45% .. +4.95%] · haut q95 +6.45% · bas q05 -6.01%
   - 60min (n=160) : retour [-6.32% .. +5.69%] · haut q95 +6.96% · bas q05 -7.64%
   - 2h (n=160) : retour [-7.46% .. +6.75%] · haut q95 +10.57% · bas q05 -8.23%
   - 4h (n=160) : retour [-7.54% .. +7.6%] · haut q95 +11.0% · bas q05 -10.16%
   - 6h (n=160) : retour [-7.72% .. +8.76%] · haut q95 +11.29% · bas q05 -10.03%
   - session (n=160) : retour [-7.74% .. +9.79%] · haut q95 +11.37% · bas q05 -10.71%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 5.0%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 65.3  _(momentum haussier)_
- **ADX** : 18.9  _(pas de tendance nette)_
- **MACD** : hist 0.233  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 26.7%
- **ATR** : 0.68 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.048  _(neutre)_
- **Vol ratio** : 1.07  _(volume normal)_
- **Choppiness** : 53.4  _(transition)_
- **MA** : MA20 8.53 · MA50 9.81 · MA200 15.67  _(prix > MA20)_
- **Dist MA** : MA20 +11.0% · MA50 -3.4% · MA200 -39.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86166 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
