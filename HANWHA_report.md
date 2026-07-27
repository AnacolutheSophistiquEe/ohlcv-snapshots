# 012450

**Generated** : 2026-07-27T00:16:59.223033+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.3 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩979000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩979000.00 (+0.4% vs entrée) · entrée ₩974712.53 · stop ₩896735.52 · T1 ₩1002777.95 · R/R 0.36  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk -0.12 _(réel 5 s)_ (GBM -0.141) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩970425.05–₩979000.00 (mid ₩974712.53)
- Spot actuel : ₩979000.00 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : ₩896735.52 (stop swing_plan-based (-4.06%))
- Targets : T1 ₩1002777.95 · R/R 0.36 | T2 ₩1030843.38 · R/R 0.72 | T3 ₩1058908.81 · R/R 1.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩896735.52


## Edge, scénarios & sizing

- EV/risk : -0.141 | EV/share : ₩-10973.652 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.12 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.2 | bear 8.6 | side 76.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.435% → cible +2.879% / stop −8.0%, p_fill 98%, n_eff≈39.5) : P(cible|rempli) **41%** · **EV/risk -0.120** (×p_fill ; si rempli -0.98% du capital)
  - **swing** (entrée dip −0.869% → cible +6.438% / stop −3.219%, p_fill 94%, n_eff≈37.4) : P(cible|rempli) **14%** · **EV/risk -0.551** (×p_fill ; si rempli -1.89% du capital)
  - **deep** (entrée dip −1.254% → cible +9.105% / stop −4.553%, p_fill 93%, n_eff≈36.9) : P(cible|rempli) **17%** · **EV/risk -0.479** (×p_fill ; si rempli -2.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→59% · +2.0%→40% · +3.0%→24% · +5.0%→12% · +8.0%→2%
- Range intraday médian 5.84% (p90 8.61%) · excursion haute méd. +1.72% / basse méd. −2.99%
- Profil de vol intra : ouverture 4.083% vs midi 1.111% vs clôture 1.131% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (144 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓1% ; spike-down 87% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.13 ; mean-reverting — autocorr -0.069)_ ; drift intra méd. -1.27% ; recovery-V 34%
- **σ réalisé intraday** 4.579% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 57% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 986212.5 (VA 972037.5–1000387.5 ; dernier close 986000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 83% · **stop −4.03%** sous le fill (sous le bruit) · cible +2.46% · R/R 0.61 (high win-rate)
- Gaps overnight (n=143) : méd. 0.78% · baisse 30% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=144) : bas méd −1.77% (p90 −4.05%) · haut méd +0.79% · range méd 2.82%
- Excursion ouverture 15min (n=144) : bas méd −2.12% (p90 −4.63%) · haut méd +1.08% · range méd 3.4%
- Excursion ouverture 30min (n=144) : bas méd −2.16% (p90 −4.94%) · haut méd +1.08% · range méd 3.95%
- Excursion ouverture 60min (n=144) : bas méd −2.38% (p90 −5.43%) · haut méd +1.29% · range méd 4.37%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 986000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 73% (103/143) · gap 21% · délai 0.2min · rebond 52% (53/103) (MFE +1.13%)
   - −1.0% : fill 30min 55% · séance 70% (99/143) · gap 17% · délai 1.1min · rebond 56% (59/99) (MFE +1.08%)
   - −1.5% : fill 30min 53% · séance 65% (92/143) · gap 10% · délai 1.7min · rebond 60% (53/92) (MFE +1.35%)
   - −2.0% : fill 30min 44% · séance 58% (76/143) · gap 7% · délai 3.6min · rebond 65% (47/76) (MFE +1.63%)
   - −3.0% : fill 30min 29% · séance 45% (55/143) · gap 2% · délai 7.1min · rebond 72% (38/55) (MFE +1.54%)
   - −4.0% : fill 30min 20% · séance 33% (41/143) · gap 2% · délai 14.0min · rebond 84% (34/41) (MFE +1.99%)
   - −5.0% : fill 30min 12% · séance 25% (30/143) · gap 1% · délai 41.9min · rebond 83% (25/30) (MFE +2.46%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.87% (p90 −2.61%) → stop au-delà de −2.12% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.41% (p90 −2.8%) → stop au-delà de −2.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.56% (p90 −2.77%) → stop au-delà de −2.67% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=678 jambes) : jambe baissière méd −1.26% (p90 −3.18%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 100% (31/31) · rebond 47% (14/31)
      · −2.0% : fill 93% (28/31) · rebond 61% (16/28)
      · −3.0% : fill 88% (25/31) · rebond 70% (17/25)
      · −4.0% : fill 73% (22/31) · rebond 87% (18/22)
      · −5.0% : fill 50% (15/31) · rebond 85% (13/15)
   - **flat** (18 séances) :
      · −1.0% : fill 87% (17/18) · rebond 48% (9/17)
      · −2.0% : fill 76% (14/18) · rebond 56% (7/14)
      · −3.0% : fill 54% (8/18) · rebond 46% (3/8)
      · −4.0% : fill 54% (8/18) · rebond 60% (5/8)
      · −5.0% : fill 52% (7/18) · rebond 66% (4/7)
   - **gap-up** (94 séances) :
      · −1.0% : fill 55% (51/94) · rebond 66% (36/51)
      · −2.0% : fill 41% (34/94) · rebond 72% (24/34)
      · −3.0% : fill 27% (22/94) · rebond 86% (18/22)
      · −4.0% : fill 14% (11/94) · rebond 100% (11/11)
      · −5.0% : fill 9% (8/94) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=144) : 35% en base · 61% si les 15 1res min sont vertes (47 cas) · 21% si rouges (97 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=144) : COUDE à **51min** → P(séance verte=clôture>ouverture) 84% si début vert vs 7% si rouge (base 35% · écart 77 pts) ; prédictivité sature ensuite (plafond brut 49min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=49) : tient le vert **84%** · continue >prix actuel 55% ; creux résiduel méd -2.08% (q20 -3.38%) → **SL/trailing à −3.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.5% → **scale +2.05% / runner +3.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **7%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.04%** (au-delà de la MAE q10 -5.04%), cible rebond +1.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=144) : retour [-5.22% .. +3.85%] · haut q95 +5.44% · bas q05 -6.4%
   - 60min (n=144) : retour [-5.13% .. +4.73%] · haut q95 +6.76% · bas q05 -7.09%
   - 2h (n=144) : retour [-6.86% .. +4.57%] · haut q95 +6.95% · bas q05 -8.01%
   - 4h (n=144) : retour [-6.48% .. +5.63%] · haut q95 +7.24% · bas q05 -8.31%
   - 6h (n=144) : retour [-6.81% .. +4.93%] · haut q95 +7.65% · bas q05 -8.4%
   - session (n=144) : retour [-6.78% .. +5.07%] · haut q95 +7.65% · bas q05 -8.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.49%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.4  _(momentum baissier)_
- **ADX** : 18.0  _(pas de tendance nette)_
- **MACD** : hist 2007.465  _(bullish_recent)_
- **BB** : %B 0.45 · largeur 37.6%
- **ATR** : 85214.29 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.144  _(distribution)_
- **Vol ratio** : 1.04  _(volume normal)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 996600.0 · MA50 1090240.0 · MA200 1143755.75  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -10.2% · MA200 -14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82736 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
