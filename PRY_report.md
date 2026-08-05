# PRY

**Generated** : 2026-08-05T21:47:04.464244+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · €122.10  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €122.10 (+1.3% vs entrée) · entrée €120.56 · stop €110.92 · T1 €123.20 · R/R 0.27  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.069 _(réel 5 s)_ (GBM -0.046) · ¼-Kelly 0.067 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €120.20–€120.93 (mid €120.56)
- Spot actuel : €122.10 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : €110.92 (stop swing_plan-based (-8.1%))
- Targets : T1 €123.20 · R/R 0.27 | T2 €124.60 · R/R 0.42 | T3 €126.01 · R/R 0.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €110.92


## Edge, scénarios & sizing

- EV/risk : -0.046 | EV/share : €-0.445 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.266 | ¼-Kelly 0.067 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.0 | bear 56.9 | side 15.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 122.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.261% → cible +2.188% / stop −8.0%, p_fill 67%, n_eff≈24.7) : P(cible|rempli) **28%** · **EV/risk -0.069** (×p_fill ; si rempli -0.83% du capital)
  - **swing** (entrée dip −2.768% → cible +3.366% / stop −5.484%, p_fill 64%, n_eff≈23.0) : P(cible|rempli) **35%** · **EV/risk -0.243** (×p_fill ; si rempli -2.08% du capital)
  - **deep** (entrée dip −4.282% → cible +4.76% / stop −8.356%, p_fill 50%, n_eff≈20.3) : P(cible|rempli) **38%** · **EV/risk -0.103** (×p_fill ; si rempli -1.71% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→61% · +2.0%→38% · +3.0%→26% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.04% (p90 6.51%) · excursion haute méd. +1.28% / basse méd. −1.79%
- Profil de vol intra : ouverture 2.365% vs midi 0.851% vs clôture 1.188% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; neutre — autocorr 0.009)_ ; drift intra méd. -1.015% ; recovery-V 18%
- **σ réalisé intraday** 2.935% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 43% / bas 72% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 116.589 (VA 115.419–117.993 ; dernier close 118.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=145) : méd. 0.3% · baisse 41% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=146) : bas méd −0.88% (p90 −2.44%) · haut méd +0.43% · range méd 1.43%
- Excursion ouverture 15min (n=146) : bas méd −0.94% (p90 −2.93%) · haut méd +0.62% · range méd 1.77%
- Excursion ouverture 30min (n=146) : bas méd −1.04% (p90 −3.24%) · haut méd +0.73% · range méd 1.94%
- Excursion ouverture 60min (n=146) : bas méd −1.23% (p90 −3.41%) · haut méd +0.86% · range méd 2.17%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 73% (106/145) · gap 28% · délai 0.2min · rebond 60% (66/106) (MFE +1.22%)
   - −1.0% : fill 30min 50% · séance 64% (90/145) · gap 21% · délai 0.3min · rebond 58% (54/90) (MFE +1.47%)
   - −1.5% : fill 30min 35% · séance 56% (78/145) · gap 17% · délai 0.4min · rebond 53% (43/78) (MFE +1.14%)
   - −2.0% : fill 30min 25% · séance 48% (64/145) · gap 11% · délai 13.0min · rebond 59% (40/64) (MFE +1.26%)
   - −3.0% : fill 30min 14% · séance 38% (47/145) · gap 4% · délai 76.9min · rebond 65% (32/47) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 22% (25/145) · gap 2% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 2% · séance 14% (17/145) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.8%) → stop au-delà de −1.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.98%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.54%) → stop au-delà de −1.01% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=455 jambes) : jambe baissière méd −1.08% (p90 −2.68%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 90% (47/52) · rebond 46% (26/47)
      · −2.0% : fill 73% (38/52) · rebond 64% (26/38)
      · −3.0% : fill 60% (29/52) · rebond 71% (22/29)
      · −4.0% : fill 38% (16/52) · rebond 65% (11/16)
      · −5.0% : fill 29% (12/52) · rebond 73% (9/12)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 46% (29/67) · rebond 71% (19/29)
      · −2.0% : fill 32% (19/67) · rebond 43% (9/19)
      · −3.0% : fill 26% (13/67) · rebond 63% (8/13)
      · −4.0% : fill 14% (6/67) · rebond 86% (5/6)
      · −5.0% : fill 6% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 46% en base · 69% si les 15 1res min sont vertes (68 cas) · 28% si rouges (78 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=146) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 83% si début vert vs 21% si rouge (base 46% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -1.3% (q20 -2.09%) → **SL/trailing à −2.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +2.48% → **scale +1.33% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **21%** (continue à baisser 68%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.13%** (au-delà de la MAE q10 -4.13%), cible rebond +1.24% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-3.03% .. +2.82%] · haut q95 +3.67% · bas q05 -3.43%
   - 60min (n=146) : retour [-3.39% .. +2.24%] · haut q95 +4.02% · bas q05 -3.59%
   - 2h (n=146) : retour [-3.85% .. +2.88%] · haut q95 +4.1% · bas q05 -4.99%
   - 4h (n=146) : retour [-3.48% .. +3.27%] · haut q95 +4.52% · bas q05 -5.04%
   - 6h (n=146) : retour [-3.81% .. +3.74%] · haut q95 +4.79% · bas q05 -5.73%
   - session (n=146) : retour [-4.76% .. +4.76%] · haut q95 +5.76% · bas q05 -6.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.8% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 35.8  _(momentum baissier)_
- **ADX** : 35.0  _(tendance etablie)_
- **MACD** : hist -0.074  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 21.3%
- **ATR** : 6.51 (95.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.043  _(neutre)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 48.9  _(transition)_
- **MA** : MA20 127.12 · MA50 138.71 · MA200 110.75  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 -12.0% · MA200 +10.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93619 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
