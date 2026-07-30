# 207940

**Generated** : 2026-07-30T00:18:38.876026+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩1479000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1479000.00 (+8.3% vs entrée) · entrée ₩1365425.00 · stop ₩1337622.95 · T1 ₩1421029.10 · R/R 2.0  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.009 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 144 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1354304.18–₩1376545.82 (mid ₩1365425.00)
- Spot actuel : ₩1479000.00 (+8.3% au-dessus de la zone — repli à attendre)
- Stop : ₩1337622.95 (stop swing_plan-based (-9.56%))
- Targets : T1 ₩1421029.10 · R/R 2.0 | T2 ₩1476633.20 · R/R 4.0 | T3 ₩1532237.29 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1337622.95


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : ₩-256.333 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 13 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 58.5 | bear 26.7 | side 14.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→51% · +2.0%→35% · +3.0%→21% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.93% (p90 6.09%) · excursion haute méd. +1.03% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.365% vs midi 0.661% vs clôture 0.796% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 12% · trend ↑2%/↓3% ; spike-down 56% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; neutre — autocorr -0.018)_ ; drift intra méd. 0.102% ; recovery-V 37%
- **σ réalisé intraday** 3.189% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 61% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 1558462.5 (VA 1536412.5–1564762.5 ; dernier close 1549000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 66% · **stop −2.7%** sous le fill (sous le bruit) · cible +1.43% · R/R 0.53 (high win-rate)
- Gaps overnight (n=141) : méd. 0.43% · baisse 32% (gap-down >1% 8% · >2% 4%)
- Excursion ouverture 5min (n=142) : bas méd −0.81% (p90 −2.4%) · haut méd +0.5% · range méd 1.61%
- Excursion ouverture 15min (n=142) : bas méd −1.03% (p90 −2.84%) · haut méd +0.61% · range méd 1.98%
- Excursion ouverture 30min (n=142) : bas méd −1.08% (p90 −3.06%) · haut méd +0.65% · range méd 2.44%
- Excursion ouverture 60min (n=142) : bas méd −1.26% (p90 −3.42%) · haut méd +0.84% · range méd 2.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1549000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 74% (95/141) · gap 20% · délai 1.2min · rebond 53% (42/95) (MFE +1.07%)
   - −1.0% : fill 30min 45% · séance 61% (76/141) · gap 8% · délai 3.0min · rebond 57% (34/76) (MFE +1.28%)
   - −1.5% : fill 30min 37% · séance 50% (59/141) · gap 5% · délai 4.4min · rebond 57% (28/59) (MFE +1.51%)
   - −2.0% : fill 30min 26% · séance 40% (50/141) · gap 4% · délai 7.3min · rebond 66% (27/50) (MFE +1.43%)
   - −3.0% : fill 30min 7% · séance 26% (31/141) · gap 2% · délai 105.3min · rebond 60% (17/31) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 14% (16/141) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 7% (9/141) · gap 1% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.45%) → stop au-delà de −1.34% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −1.97%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −2.31%) → stop au-delà de −1.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=350 jambes) : jambe baissière méd −1.11% (p90 −2.64%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (32 séances) :
      · −1.0% : fill 98% (31/32) · rebond 70% (16/31)
      · −2.0% : fill 79% (26/32) · rebond 68% (13/26)
      · −3.0% : fill 37% (13/32) · rebond 57% (7/13)
      · −4.0% : fill 22% (7/32) · rebond 58% (3/7)
      · −5.0% : fill 9% (4/32) · rebond 100% (4/4)
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
- **P(clôture VERTE) selon le drive 15min** (n=142) : 41% en base · 66% si les 15 1res min sont vertes (50 cas) · 25% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=142) : COUDE à **33min** → P(séance verte=clôture>ouverture) 71% si début vert vs 23% si rouge (base 41% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=51) : tient le vert **71%** · continue >prix actuel 36% ; creux résiduel méd -1.48% (q20 -2.69%) → **SL/trailing à −2.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.87% → **scale +0.97% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **23%** (continue à baisser 53%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.27%** (au-delà de la MAE q10 -3.27%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-3.02% .. +3.52%] · haut q95 +3.98% · bas q05 -3.52%
   - 60min (n=142) : retour [-3.48% .. +3.02%] · haut q95 +4.5% · bas q05 -3.77%
   - 2h (n=142) : retour [-4.35% .. +3.55%] · haut q95 +5.1% · bas q05 -4.79%
   - 4h (n=142) : retour [-5.15% .. +4.3%] · haut q95 +5.15% · bas q05 -5.41%
   - 6h (n=142) : retour [-5.17% .. +4.45%] · haut q95 +5.78% · bas q05 -5.96%
   - session (n=142) : retour [-4.87% .. +3.98%] · haut q95 +5.78% · bas q05 -5.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.04%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 13.6  _(pas de tendance nette)_
- **MACD** : hist 15812.199  _(bullish_recent)_
- **BB** : %B 0.76 · largeur 17.6%
- **ATR** : 78785.71 (96.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.081  _(accumulation)_
- **Vol ratio** : 1.41  _(volume normal)_
- **Choppiness** : 53.2  _(transition)_
- **MA** : MA20 1413100.0 · MA50 1377960.0 · MA200 1611424.13  _(prix > MA20)_
- **Dist MA** : MA20 +4.7% · MA50 +7.3% · MA200 -8.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80137 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
