# 267260

**Generated** : 2026-08-07T21:51:39.706394+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩762000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩762000.00 (+0.8% vs entrée) · entrée ₩756127.70 · stop ₩695637.48 · T1 ₩838415.28 · R/R 1.36  
> ↳ P(T1 av. stop) 1 % _(réel 5 s)_ · EV/risk -0.135 _(réel 5 s)_ (GBM -0.178) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩750255.39–₩762000.00 (mid ₩756127.70)
- Spot actuel : ₩762000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩695637.48 (stop swing_plan-based (-11.22%))
- Targets : T1 ₩838415.28 · R/R 1.36 | T2 ₩845154.36 · R/R 1.47 | T3 ₩851893.44 · R/R 1.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩695637.48


## Edge, scénarios & sizing

- EV/risk : -0.178 | EV/share : ₩-10782.381 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.02 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 77.2 | side 16.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.772% → cible +10.883% / stop −8.0%, p_fill 98%, n_eff≈39.6) : P(cible|rempli) **1%** · **EV/risk -0.135** (×p_fill ; si rempli -1.10% du capital)
  - **swing** (entrée dip −1.706% → cible +9.44% / stop −9.679%, p_fill 93%, n_eff≈37.5) : P(cible|rempli) **31%** · **EV/risk -0.277** (×p_fill ; si rempli -2.88% du capital)
  - **deep** (entrée dip −2.498% → cible +13.35% / stop −14.637%, p_fill 91%, n_eff≈36.7) : P(cible|rempli) **27%** · **EV/risk -0.366** (×p_fill ; si rempli -5.86% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→70% · +2.0%→48% · +3.0%→36% · +5.0%→12% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.58%) · excursion haute méd. +1.85% / basse méd. −3.81%
- Profil de vol intra : ouverture 4.419% vs midi 1.21% vs clôture 1.24% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (149 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. -1.676% ; recovery-V 25%
- **σ réalisé intraday** 4.939% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 69% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 759437.5 (VA 753312.5–766787.5 ; dernier close 758000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 82% · **stop −4.53%** sous le fill (sous le bruit) · cible +2.54% · R/R 0.56 (high win-rate)
- Gaps overnight (n=148) : méd. 1.12% · baisse 40% (gap-down >1% 23% · >2% 12%)
- Excursion ouverture 5min (n=149) : bas méd −1.71% (p90 −4.2%) · haut méd +1.05% · range méd 2.93%
- Excursion ouverture 15min (n=149) : bas méd −1.95% (p90 −4.75%) · haut méd +1.17% · range méd 3.59%
- Excursion ouverture 30min (n=149) : bas méd −2.26% (p90 −5.14%) · haut méd +1.38% · range méd 3.95%
- Excursion ouverture 60min (n=149) : bas méd −2.86% (p90 −5.71%) · haut méd +1.45% · range méd 4.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 758000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 70% (104/148) · gap 32% · délai 0.0min · rebond 54% (58/104) (MFE +1.21%)
   - −1.0% : fill 30min 55% · séance 68% (97/148) · gap 23% · délai 0.1min · rebond 59% (58/97) (MFE +1.34%)
   - −1.5% : fill 30min 48% · séance 62% (84/148) · gap 16% · délai 0.4min · rebond 67% (55/84) (MFE +1.28%)
   - −2.0% : fill 30min 44% · séance 58% (76/148) · gap 12% · délai 0.7min · rebond 70% (52/76) (MFE +1.73%)
   - −3.0% : fill 30min 33% · séance 50% (61/148) · gap 7% · délai 2.8min · rebond 78% (43/61) (MFE +2.17%)
   - −4.0% : fill 30min 23% · séance 41% (50/148) · gap 4% · délai 15.0min · rebond 76% (39/50) (MFE +2.34%)
   - −5.0% : fill 30min 16% · séance 35% (40/148) · gap 1% · délai 39.2min · rebond 82% (31/40) (MFE +2.54%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.6%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.68%) → stop au-delà de −2.63% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.26% (p90 −5.02%) → stop au-delà de −3.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=763 jambes) : jambe baissière méd −1.28% (p90 −3.6%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 98% (51/52) · rebond 55% (28/51)
      · −2.0% : fill 93% (44/52) · rebond 66% (27/44)
      · −3.0% : fill 85% (38/52) · rebond 78% (26/38)
      · −4.0% : fill 73% (33/52) · rebond 75% (26/33)
      · −5.0% : fill 65% (26/52) · rebond 82% (20/26)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (79 séances) :
      · −1.0% : fill 44% (32/79) · rebond 69% (23/32)
      · −2.0% : fill 31% (20/79) · rebond 74% (16/20)
      · −3.0% : fill 22% (12/79) · rebond 77% (9/12)
      · −4.0% : fill 18% (10/79) · rebond 82% (8/10)
      · −5.0% : fill 13% (7/79) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=149) : 34% en base · 50% si les 15 1res min sont vertes (68 cas) · 25% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=149) : COUDE à **1:19** → P(séance verte=clôture>ouverture) 70% si début vert vs 11% si rouge (base 34% · écart 58 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **70%** · continue >prix actuel 42% ; creux résiduel méd -1.81% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.45% / q75 +3.02% → **scale +1.45% / runner +3.02%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **11%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.66%** (au-delà de la MAE q10 -5.66%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=149) : retour [-5.48% .. +2.69%] · haut q95 +4.21% · bas q05 -5.79%
   - 60min (n=149) : retour [-5.69% .. +2.85%] · haut q95 +4.44% · bas q05 -6.41%
   - 2h (n=149) : retour [-7.04% .. +3.69%] · haut q95 +5.14% · bas q05 -7.75%
   - 4h (n=149) : retour [-6.95% .. +3.9%] · haut q95 +5.4% · bas q05 -8.72%
   - 6h (n=149) : retour [-8.22% .. +4.38%] · haut q95 +6.58% · bas q05 -9.4%
   - session (n=149) : retour [-7.64% .. +4.2%] · haut q95 +6.68% · bas q05 -9.68%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 50.8  _(neutre)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 13323.784  _(bullish_recent)_
- **BB** : %B 0.52 · largeur 40.8%
- **ATR** : 72500.0 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.037  _(neutre)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 42.3  _(transition)_
- **MA** : MA20 754950.0 · MA50 896680.0 · MA200 924222.2  _(prix > MA20)_
- **Dist MA** : MA20 +0.9% · MA50 -15.0% · MA200 -17.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82188 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
