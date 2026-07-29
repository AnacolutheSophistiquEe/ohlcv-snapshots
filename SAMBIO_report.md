# 207940

**Generated** : 2026-07-29T00:18:39.808566+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1549000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩1549000.00 (+4.7% vs entrée) · entrée ₩1479875.00 · stop ₩1361485.00 · T1 ₩1506460.66 · R/R 0.22  
> ↳ P(T1 av. stop) 37 % · EV/risk -0.061 · ¼-Kelly 0.059 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 176 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1474557.87–₩1485192.13 (mid ₩1479875.00)
- Spot actuel : ₩1549000.00 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1361485.00 (stop swing_plan-based (-11.63%))
- Targets : T1 ₩1506460.66 · R/R 0.22 | T2 ₩1533046.33 · R/R 0.45 | T3 ₩1559631.99 · R/R 0.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1361485.00


## Edge, scénarios & sizing

- EV/risk : -0.061 | EV/share : ₩-7271.020 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 13 % | T3 6 %
- Kelly (position) : f* 0.237 | ¼-Kelly 0.059 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 17.6 | side 76.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→51% · +2.0%→35% · +3.0%→22% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.9% (p90 6.09%) · excursion haute méd. +1.03% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.375% vs midi 0.652% vs clôture 0.788% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 12% · trend ↑2%/↓3% ; spike-down 57% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.148 ; neutre — autocorr -0.016)_ ; drift intra méd. 0.058% ; recovery-V 33%
- **σ réalisé intraday** 3.173% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 59% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 1544975.0 (VA 1538525.0–1551425.0 ; dernier close 1541500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 66% · **stop −2.7%** sous le fill (sous le bruit) · cible +1.43% · R/R 0.53 (high win-rate)
- Gaps overnight (n=140) : méd. 0.43% · baisse 31% (gap-down >1% 8% · >2% 4%)
- Excursion ouverture 5min (n=141) : bas méd −0.84% (p90 −2.4%) · haut méd +0.5% · range méd 1.55%
- Excursion ouverture 15min (n=141) : bas méd −1.06% (p90 −2.85%) · haut méd +0.58% · range méd 1.96%
- Excursion ouverture 30min (n=141) : bas méd −1.09% (p90 −3.07%) · haut méd +0.63% · range méd 2.41%
- Excursion ouverture 60min (n=141) : bas méd −1.26% (p90 −3.45%) · haut méd +0.81% · range méd 2.7%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1541500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 74% (94/140) · gap 18% · délai 1.2min · rebond 52% (41/94) (MFE +1.03%)
   - −1.0% : fill 30min 46% · séance 61% (75/140) · gap 8% · délai 2.5min · rebond 56% (33/75) (MFE +1.14%)
   - −1.5% : fill 30min 38% · séance 49% (58/140) · gap 5% · délai 3.7min · rebond 55% (27/58) (MFE +1.44%)
   - −2.0% : fill 30min 26% · séance 41% (50/140) · gap 4% · délai 7.3min · rebond 66% (27/50) (MFE +1.43%)
   - −3.0% : fill 30min 7% · séance 26% (31/140) · gap 2% · délai 105.3min · rebond 60% (17/31) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 15% (16/140) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 8% (9/140) · gap 1% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.78% (p90 −2.45%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.01%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −2.31%) → stop au-delà de −1.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=345 jambes) : jambe baissière méd −1.1% (p90 −2.64%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (31 séances) :
      · −1.0% : fill 98% (30/31) · rebond 67% (15/30)
      · −2.0% : fill 86% (26/31) · rebond 68% (13/26)
      · −3.0% : fill 41% (13/31) · rebond 57% (7/13)
      · −4.0% : fill 24% (7/31) · rebond 58% (3/7)
      · −5.0% : fill 10% (4/31) · rebond 100% (4/4)
   - **flat** (42 séances) :
      · −1.0% : fill 64% (23/42) · rebond 31% (7/23)
      · −2.0% : fill 36% (10/42) · rebond 57% (5/10)
      · −3.0% : fill 28% (7/42) · rebond 97% (6/7)
      · −4.0% : fill 16% (4/42) · rebond 100% (4/4)
      · −5.0% : fill 7% (2/42) · rebond 89% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 44% (22/67) · rebond 63% (11/22)
      · −2.0% : fill 24% (14/67) · rebond 68% (9/14)
      · −3.0% : fill 20% (11/67) · rebond 40% (4/11)
      · −4.0% : fill 10% (5/67) · rebond 33% (2/5)
      · −5.0% : fill 7% (3/67) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 40% en base · 65% si les 15 1res min sont vertes (49 cas) · 25% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=141) : COUDE à **33min** → P(séance verte=clôture>ouverture) 70% si début vert vs 23% si rouge (base 40% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=50) : tient le vert **70%** · continue >prix actuel 38% ; creux résiduel méd -1.41% (q20 -2.64%) → **SL/trailing à −2.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.14% / q75 +2.0% → **scale +1.14% / runner +2.0%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **23%** (continue à baisser 53%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.27%** (au-delà de la MAE q10 -3.27%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-3.03% .. +3.52%] · haut q95 +3.99% · bas q05 -3.53%
   - 60min (n=141) : retour [-3.52% .. +3.05%] · haut q95 +4.55% · bas q05 -3.81%
   - 2h (n=141) : retour [-4.37% .. +3.65%] · haut q95 +5.12% · bas q05 -4.81%
   - 4h (n=141) : retour [-5.21% .. +4.31%] · haut q95 +5.15% · bas q05 -5.44%
   - 6h (n=141) : retour [-5.21% .. +4.63%] · haut q95 +5.84% · bas q05 -6.03%
   - session (n=141) : retour [-4.89% .. +4.06%] · haut q95 +5.85% · bas q05 -6.04%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.03%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.9  _(momentum haussier)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist 19059.789  _(bullish_recent)_
- **BB** : %B 1.08 · largeur 17.2%
- **ATR** : 75642.86 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.061  _(accumulation)_
- **Vol ratio** : 2.45  _(volume au-dessus de la moyenne)_
- **Choppiness** : 51.6  _(transition)_
- **MA** : MA20 1408700.0 · MA50 1376760.0 · MA200 1611739.87  _(prix > MA20)_
- **Dist MA** : MA20 +10.0% · MA50 +12.5% · MA200 -3.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (81424 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
