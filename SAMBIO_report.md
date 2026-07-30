# 207940

**Generated** : 2026-07-30T21:54:49.219232+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩1527000.00  

> ⛔ **STAND-DOWN** — mise optimale nulle (Kelly ≤ 0) — edge trop ténu pour s'engager (EV blended à peine positive ; cf. badge pour la méthode/n des probas)  
> ↳ spot ₩1527000.00 (+10.1% vs entrée) · entrée ₩1387025.00 · stop ₩1358253.75 · T1 ₩1444567.49 · R/R 2.0  
> ↳ P(T1 av. stop) 27 % · EV/risk 0.013 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 168 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1375516.50–₩1398533.50 (mid ₩1387025.00)
- Spot actuel : ₩1527000.00 (+10.1% au-dessus de la zone — repli à attendre)
- Stop : ₩1358253.75 (stop swing_plan-based (-11.05%))
- Targets : T1 ₩1444567.49 · R/R 2.0 | T2 ₩1502109.98 · R/R 4.0 | T3 ₩1559652.48 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1358253.75


## Edge, scénarios & sizing

- EV/risk : 0.013 | EV/share : ₩383.880 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 13 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.8 | bear 22.2 | side 25.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→52% · +2.0%→35% · +3.0%→21% · +5.0%→6% · +8.0%→2%
- Range intraday médian 3.93% (p90 6.17%) · excursion haute méd. +1.06% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.39% vs midi 0.685% vs clôture 0.816% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 12% · trend ↑2%/↓3% ; spike-down 57% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.142 ; neutre — autocorr -0.028)_ ; drift intra méd. -0.094% ; recovery-V 35%
- **σ réalisé intraday** 3.306% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 63% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 1468075.0 (VA 1436575.0–1499575.0 ; dernier close 1479000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 16% · rebond 64% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=142) : méd. 0.4% · baisse 33% (gap-down >1% 8% · >2% 4%)
- Excursion ouverture 5min (n=143) : bas méd −0.84% (p90 −2.51%) · haut méd +0.5% · range méd 1.62%
- Excursion ouverture 15min (n=143) : bas méd −1.06% (p90 −2.94%) · haut méd +0.64% · range méd 2.0%
- Excursion ouverture 30min (n=143) : bas méd −1.09% (p90 −3.14%) · haut méd +0.68% · range méd 2.46%
- Excursion ouverture 60min (n=143) : bas méd −1.26% (p90 −3.49%) · haut méd +0.85% · range méd 2.77%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1479000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 75% (96/142) · gap 20% · délai 1.1min · rebond 54% (43/96) (MFE +1.07%)
   - −1.0% : fill 30min 46% · séance 62% (77/142) · gap 8% · délai 2.5min · rebond 59% (35/77) (MFE +1.29%)
   - −1.5% : fill 30min 38% · séance 51% (60/142) · gap 5% · délai 3.7min · rebond 59% (29/60) (MFE +1.6%)
   - −2.0% : fill 30min 27% · séance 41% (51/142) · gap 4% · délai 6.9min · rebond 67% (28/51) (MFE +1.48%)
   - −3.0% : fill 30min 9% · séance 27% (32/142) · gap 2% · délai 92.6min · rebond 63% (18/32) (MFE +1.4%)
   - −4.0% : fill 30min 4% · séance 16% (17/142) · gap 2% · délai 90.8min · rebond 64% (10/17) (MFE +1.37%)
   - −5.0% : fill 30min 2% · séance 9% (10/142) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.63% (p90 −2.42%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −1.97%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −2.31%) → stop au-delà de −1.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=357 jambes) : jambe baissière méd −1.13% (p90 −2.76%) · ~8.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 98% (32/33) · rebond 72% (17/32)
      · −2.0% : fill 81% (27/33) · rebond 71% (14/27)
      · −3.0% : fill 42% (14/33) · rebond 64% (8/14)
      · −4.0% : fill 28% (8/33) · rebond 70% (4/8)
      · −5.0% : fill 16% (5/33) · rebond 100% (5/5)
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
- **P(clôture VERTE) selon le drive 15min** (n=143) : 40% en base · 66% si les 15 1res min sont vertes (50 cas) · 24% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=143) : COUDE à **33min** → P(séance verte=clôture>ouverture) 71% si début vert vs 23% si rouge (base 40% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=51) : tient le vert **71%** · continue >prix actuel 36% ; creux résiduel méd -1.48% (q20 -2.69%) → **SL/trailing à −2.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.87% → **scale +0.97% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **23%** (continue à baisser 54%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.48%** (au-delà de la MAE q10 -3.48%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-3.02% .. +3.51%] · haut q95 +3.98% · bas q05 -3.53%
   - 60min (n=143) : retour [-3.45% .. +2.99%] · haut q95 +4.46% · bas q05 -3.73%
   - 2h (n=143) : retour [-4.33% .. +3.54%] · haut q95 +5.08% · bas q05 -4.78%
   - 4h (n=143) : retour [-5.23% .. +4.29%] · haut q95 +5.14% · bas q05 -5.86%
   - 6h (n=143) : retour [-5.13% .. +4.27%] · haut q95 +5.74% · bas q05 -6.18%
   - session (n=143) : retour [-4.85% .. +3.95%] · haut q95 +5.74% · bas q05 -6.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.06%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 68.2  _(momentum haussier)_
- **ADX** : 13.5  _(pas de tendance nette)_
- **MACD** : hist 15873.798  _(pas de croisement recent)_
- **BB** : %B 0.9 · largeur 18.9%
- **ATR** : 80500.0 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.114  _(accumulation)_
- **Vol ratio** : 1.26  _(volume normal)_
- **Choppiness** : 58.3  _(transition)_
- **MA** : MA20 1419650.0 · MA50 1380780.0 · MA200 1611394.51  _(prix > MA20)_
- **Dist MA** : MA20 +7.6% · MA50 +10.6% · MA200 -5.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (80337 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
