# 012450

**Generated** : 2026-07-17T00:19:20.053262+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩943000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩943000.00 (+1.2% vs entrée) · entrée ₩932175.57 · stop ₩857601.53 · T1 ₩956904.50 · R/R 0.33  
> ↳ P(T1 av. stop) 34 % _(réel 5 s)_ · EV/risk -0.122 _(réel 5 s)_ (GBM -0.146) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩927229.79–₩937121.36 (mid ₩932175.57)
- Spot actuel : ₩943000.00 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : ₩857601.53 (stop swing_plan-based (-5.42%))
- Targets : T1 ₩956904.50 · R/R 0.33 | T2 ₩981633.43 · R/R 0.66 | T3 ₩1006362.36 · R/R 0.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩857601.53


## Edge, scénarios & sizing

- EV/risk : -0.146 | EV/share : ₩-10882.956 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.12 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.1 | bear 73.3 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.152% → cible +2.653% / stop −8.0%, p_fill 91%, n_eff≈36.5) : P(cible|rempli) **34%** · **EV/risk -0.122** (×p_fill ; si rempli -1.07% du capital)
  - **swing** (entrée dip −2.529% → cible +5.932% / stop −2.966%, p_fill 80%, n_eff≈31.5) : P(cible|rempli) **25%** · **EV/risk -0.238** (×p_fill ; si rempli -0.88% du capital)
  - **deep** (entrée dip −3.899% → cible +8.389% / stop −4.194%, p_fill 81%, n_eff≈31.3) : P(cible|rempli) **21%** · **EV/risk -0.363** (×p_fill ; si rempli -1.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→57% · +2.0%→39% · +3.0%→22% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.6% (p90 8.37%) · excursion haute méd. +1.66% / basse méd. −3.37%
- Profil de vol intra : ouverture 4.044% vs midi 1.085% vs clôture 1.126% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 87% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.138 ; mean-reverting — autocorr -0.049)_ ; drift intra méd. -2.082% ; recovery-V 23%
- **σ réalisé intraday** 4.537% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 34% / bas 58% / whipsaw 6%
- POC intraday (dernière séance, temps-au-prix) : 925625.0 (VA 914825.0–944525.0 ; dernier close 926000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 82% · **stop −4.1%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.54 (high win-rate)
- Gaps overnight (n=136) : méd. 0.97% · baisse 28% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=137) : bas méd −1.73% (p90 −4.05%) · haut méd +0.79% · range méd 2.72%
- Excursion ouverture 15min (n=137) : bas méd −2.06% (p90 −4.78%) · haut méd +0.86% · range méd 3.42%
- Excursion ouverture 30min (n=137) : bas méd −2.5% (p90 −5.21%) · haut méd +1.05% · range méd 3.97%
- Excursion ouverture 60min (n=137) : bas méd −2.6% (p90 −5.66%) · haut méd +1.27% · range méd 4.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 926000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 74% (98/136) · gap 20% · délai 0.5min · rebond 49% (49/98) (MFE +0.73%)
   - −1.0% : fill 30min 55% · séance 72% (95/136) · gap 16% · délai 1.2min · rebond 55% (56/95) (MFE +1.01%)
   - −1.5% : fill 30min 52% · séance 67% (88/136) · gap 9% · délai 2.2min · rebond 58% (50/88) (MFE +1.25%)
   - −2.0% : fill 30min 44% · séance 58% (72/136) · gap 6% · délai 4.5min · rebond 64% (44/72) (MFE +1.47%)
   - −3.0% : fill 30min 29% · séance 48% (53/136) · gap 3% · délai 9.2min · rebond 74% (37/53) (MFE +1.54%)
   - −4.0% : fill 30min 21% · séance 34% (39/136) · gap 2% · délai 14.1min · rebond 82% (32/39) (MFE +1.99%)
   - −5.0% : fill 30min 11% · séance 26% (29/136) · gap 2% · délai 45.4min · rebond 82% (24/29) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −2.39%) → stop au-delà de −2.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.91%) → stop au-delà de −2.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.37% (p90 −2.89%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=629 jambes) : jambe baissière méd −1.29% (p90 −3.39%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (29 séances) :
      · −1.0% : fill 100% (29/29) · rebond 47% (13/29)
      · −2.0% : fill 91% (26/29) · rebond 63% (15/26)
      · −3.0% : fill 86% (23/29) · rebond 74% (16/23)
      · −4.0% : fill 68% (20/29) · rebond 83% (16/20)
      · −5.0% : fill 50% (14/29) · rebond 83% (12/14)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 48% (9/17)
      · −2.0% : fill 87% (14/17) · rebond 56% (7/14)
      · −3.0% : fill 63% (8/17) · rebond 46% (3/8)
      · −4.0% : fill 63% (8/17) · rebond 60% (5/8)
      · −5.0% : fill 60% (7/17) · rebond 66% (4/7)
   - **gap-up** (90 séances) :
      · −1.0% : fill 56% (49/90) · rebond 62% (34/49)
      · −2.0% : fill 40% (32/90) · rebond 67% (22/32)
      · −3.0% : fill 31% (22/90) · rebond 86% (18/22)
      · −4.0% : fill 16% (11/90) · rebond 100% (11/11)
      · −5.0% : fill 11% (8/90) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 30% en base · 54% si les 15 1res min sont vertes (44 cas) · 17% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=137) : COUDE à **51min** → P(séance verte=clôture>ouverture) 79% si début vert vs 7% si rouge (base 30% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=44) : tient le vert **79%** · continue >prix actuel 53% ; creux résiduel méd -1.88% (q20 -3.38%) → **SL/trailing à −3.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.56% / q75 +2.99% → **scale +1.56% / runner +2.99%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **7%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.14%** (au-delà de la MAE q10 -5.14%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-5.7% .. +3.99%] · haut q95 +5.61% · bas q05 -7.05%
   - 60min (n=137) : retour [-5.28% .. +4.14%] · haut q95 +6.28% · bas q05 -7.31%
   - 2h (n=137) : retour [-7.05% .. +3.75%] · haut q95 +6.28% · bas q05 -8.12%
   - 4h (n=137) : retour [-6.85% .. +5.52%] · haut q95 +7.07% · bas q05 -8.59%
   - 6h (n=137) : retour [-6.83% .. +4.25%] · haut q95 +7.15% · bas q05 -8.51%
   - session (n=137) : retour [-6.96% .. +4.65%] · haut q95 +7.15% · bas q05 -8.51%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.5  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -12139.598  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 33.4%
- **ATR** : 89642.86 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.154  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 45.5  _(transition)_
- **MA** : MA20 1040650.0 · MA50 1131320.0 · MA200 1146229.05  _(prix < MA20)_
- **Dist MA** : MA20 -9.4% · MA50 -16.6% · MA200 -17.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81801 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
