# 012450

**Generated** : 2026-07-21T00:17:38.916259+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩875000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩875000.00 (+2.1% vs entrée) · entrée ₩857120.69 · stop ₩788551.04 · T1 ₩899702.30 · R/R 0.62  
> ↳ P(T1 av. stop) 21 % _(réel 5 s)_ · EV/risk -0.069 _(réel 5 s)_ (GBM -0.144) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩852466.25–₩861775.13 (mid ₩857120.69)
- Spot actuel : ₩875000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩788551.04 (stop swing_plan-based (-7.64%))
- Targets : T1 ₩899702.30 · R/R 0.62 | T2 ₩913214.01 · R/R 0.82 | T3 ₩926725.73 · R/R 1.02
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩788551.04


## Edge, scénarios & sizing

- EV/risk : -0.144 | EV/share : ₩-9896.323 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.049 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.0 | bear 73.3 | side 8.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.043% → cible +4.968% / stop −8.0%, p_fill 80%, n_eff≈32.1) : P(cible|rempli) **21%** · **EV/risk -0.069** (×p_fill ; si rempli -0.68% du capital)
  - **swing** (entrée dip −4.493% → cible +6.053% / stop −3.295%, p_fill 65%, n_eff≈24.6) : P(cible|rempli) **19%** · **EV/risk -0.299** (×p_fill ; si rempli -1.52% du capital)
  - **deep** (entrée dip −6.947% → cible +8.56% / stop −4.28%, p_fill 58%, n_eff≈22.5) : P(cible|rempli) **29%** · **EV/risk -0.119** (×p_fill ; si rempli -0.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→60% · +2.0%→41% · +3.0%→25% · +5.0%→10% · +8.0%→2%
- Range intraday médian 5.71% (p90 8.37%) · excursion haute méd. +1.79% / basse méd. −3.04%
- Profil de vol intra : ouverture 4.055% vs midi 1.098% vs clôture 1.138% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (139 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 88% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. -1.766% ; recovery-V 30%
- **σ réalisé intraday** 4.617% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 62% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 944812.5 (VA 926937.5–951312.5 ; dernier close 943000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 83% · **stop −4.84%** sous le fill (sous le bruit) · cible +2.11% · R/R 0.44 (high win-rate)
- Gaps overnight (n=138) : méd. 0.82% · baisse 29% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=139) : bas méd −1.78% (p90 −4.05%) · haut méd +0.77% · range méd 2.81%
- Excursion ouverture 15min (n=139) : bas méd −2.13% (p90 −4.69%) · haut méd +1.02% · range méd 3.38%
- Excursion ouverture 30min (n=139) : bas méd −2.2% (p90 −5.1%) · haut méd +1.08% · range méd 3.91%
- Excursion ouverture 60min (n=139) : bas méd −2.45% (p90 −5.57%) · haut méd +1.28% · range méd 4.28%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 943000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 75% (100/138) · gap 21% · délai 0.3min · rebond 51% (51/100) (MFE +1.05%)
   - −1.0% : fill 30min 57% · séance 73% (97/138) · gap 17% · délai 1.1min · rebond 57% (58/97) (MFE +1.07%)
   - −1.5% : fill 30min 54% · séance 68% (90/138) · gap 8% · délai 2.0min · rebond 61% (52/90) (MFE +1.34%)
   - −2.0% : fill 30min 45% · séance 60% (74/138) · gap 6% · délai 4.5min · rebond 66% (46/74) (MFE +1.63%)
   - −3.0% : fill 30min 30% · séance 48% (54/138) · gap 3% · délai 8.0min · rebond 75% (38/54) (MFE +1.55%)
   - −4.0% : fill 30min 20% · séance 35% (40/138) · gap 2% · délai 17.6min · rebond 83% (33/40) (MFE +2.11%)
   - −5.0% : fill 30min 11% · séance 25% (29/138) · gap 1% · délai 45.4min · rebond 82% (24/29) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.21%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.41% (p90 −2.89%) → stop au-delà de −2.67% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.67% (p90 −2.86%) → stop au-delà de −2.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=645 jambes) : jambe baissière méd −1.29% (p90 −3.28%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 100% (30/30) · rebond 51% (14/30)
      · −2.0% : fill 92% (27/30) · rebond 66% (16/27)
      · −3.0% : fill 87% (24/30) · rebond 76% (17/24)
      · −4.0% : fill 71% (21/30) · rebond 85% (17/21)
      · −5.0% : fill 46% (14/30) · rebond 83% (12/14)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 48% (9/17)
      · −2.0% : fill 87% (14/17) · rebond 56% (7/14)
      · −3.0% : fill 63% (8/17) · rebond 46% (3/8)
      · −4.0% : fill 63% (8/17) · rebond 60% (5/8)
      · −5.0% : fill 60% (7/17) · rebond 66% (4/7)
   - **gap-up** (91 séances) :
      · −1.0% : fill 57% (50/91) · rebond 64% (35/50)
      · −2.0% : fill 42% (33/91) · rebond 70% (23/33)
      · −3.0% : fill 30% (22/91) · rebond 86% (18/22)
      · −4.0% : fill 16% (11/91) · rebond 100% (11/11)
      · −5.0% : fill 10% (8/91) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=139) : 33% en base · 59% si les 15 1res min sont vertes (46 cas) · 17% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=139) : COUDE à **51min** → P(séance verte=clôture>ouverture) 81% si début vert vs 7% si rouge (base 33% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=46) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -2.3% (q20 -3.35%) → **SL/trailing à −3.35%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +3.4% → **scale +1.8% / runner +3.4%**, sortie à la clôture
  - **si ROUGE au coude** (n=93) : edge inversé — récupère vert seulement **7%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.14%** (au-delà de la MAE q10 -5.14%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=139) : retour [-5.62% .. +3.95%] · haut q95 +5.57% · bas q05 -6.87%
   - 60min (n=139) : retour [-5.24% .. +3.8%] · haut q95 +6.17% · bas q05 -7.22%
   - 2h (n=139) : retour [-7.0% .. +3.72%] · haut q95 +6.17% · bas q05 -8.08%
   - 4h (n=139) : retour [-6.75% .. +5.52%] · haut q95 +7.0% · bas q05 -8.51%
   - 6h (n=139) : retour [-6.82% .. +4.19%] · haut q95 +7.13% · bas q05 -8.48%
   - session (n=139) : retour [-6.91% .. +4.64%] · haut q95 +7.13% · bas q05 -8.48%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.36%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.3  _(momentum baissier)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist -13741.987  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 35.8%
- **ATR** : 91785.71 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.182  _(distribution)_
- **Vol ratio** : 1.79  _(volume au-dessus de la moyenne)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 1028300.0 · MA50 1120160.0 · MA200 1145495.49  _(prix < MA20)_
- **Dist MA** : MA20 -14.9% · MA50 -21.9% · MA200 -23.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82494 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
