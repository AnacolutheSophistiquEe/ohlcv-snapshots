# 207940

**Generated** : 2026-07-28T00:17:27.601807+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1545000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩1545000.00 (+4.6% vs entrée) · entrée ₩1476875.00 · stop ₩1358725.00 · T1 ₩1506425.97 · R/R 0.25  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.066 · ¼-Kelly 0.051 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 173 % hors [0,100] (R² max 0.64). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 1.18 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1470964.81–₩1482785.19 (mid ₩1476875.00)
- Spot actuel : ₩1545000.00 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : ₩1358725.00 (stop swing_plan-based (-11.72%))
- Targets : T1 ₩1506425.97 · R/R 0.25 | T2 ₩1535976.93 · R/R 0.5 | T3 ₩1565527.90 · R/R 0.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1358725.00


## Edge, scénarios & sizing

- EV/risk : -0.066 | EV/share : ₩-7846.271 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 9 % | T3 5 %
- Kelly (position) : f* 0.205 | ¼-Kelly 0.051 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.4 | bear 17.5 | side 76.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=9, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→69% · +1.0%→51% · +2.0%→34% · +3.0%→21% · +5.0%→5% · +8.0%→2%
- Range intraday médian 3.87% (p90 6.09%) · excursion haute méd. +1.03% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.327% vs midi 0.652% vs clôture 0.784% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 12% · trend ↑2%/↓3% ; spike-down 59% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.147 ; neutre — autocorr -0.017)_ ; drift intra méd. -0.077% ; recovery-V 33%
- **σ réalisé intraday** 3.146% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 62% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 1511487.5 (VA 1503637.5–1531112.5 ; dernier close 1518000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 27% · rebond 60% · **stop −2.29%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.61 (high win-rate)
- Gaps overnight (n=139) : méd. 0.44% · baisse 29% (gap-down >1% 6% · >2% 4%)
- Excursion ouverture 5min (n=140) : bas méd −0.81% (p90 −2.4%) · haut méd +0.48% · range méd 1.53%
- Excursion ouverture 15min (n=140) : bas méd −1.07% (p90 −2.87%) · haut méd +0.55% · range méd 1.93%
- Excursion ouverture 30min (n=140) : bas méd −1.13% (p90 −3.08%) · haut méd +0.59% · range méd 2.35%
- Excursion ouverture 60min (n=140) : bas méd −1.28% (p90 −3.47%) · haut méd +0.73% · range méd 2.68%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1518000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 73% (93/139) · gap 17% · délai 1.3min · rebond 50% (40/93) (MFE +1.01%)
   - −1.0% : fill 30min 45% · séance 60% (74/139) · gap 6% · délai 3.0min · rebond 55% (32/74) (MFE +1.09%)
   - −1.5% : fill 30min 37% · séance 48% (57/139) · gap 5% · délai 4.4min · rebond 54% (26/57) (MFE +1.38%)
   - −2.0% : fill 30min 25% · séance 40% (49/139) · gap 4% · délai 8.9min · rebond 64% (26/49) (MFE +1.34%)
   - −3.0% : fill 30min 8% · séance 27% (31/139) · gap 2% · délai 105.3min · rebond 60% (17/31) (MFE +1.39%)
   - −4.0% : fill 30min 4% · séance 15% (16/139) · gap 2% · délai 73.7min · rebond 60% (9/16) (MFE +1.72%)
   - −5.0% : fill 30min 2% · séance 8% (9/139) · gap 1% · délai 190.8min · rebond 65% (6/9) (MFE +1.55%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.45%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.04%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.07% (p90 −2.38%) → stop au-delà de −1.8% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=340 jambes) : jambe baissière méd −1.1% (p90 −2.65%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (30 séances) :
      · −1.0% : fill 98% (29/30) · rebond 64% (14/29)
      · −2.0% : fill 85% (25/30) · rebond 65% (12/25)
      · −3.0% : fill 44% (13/30) · rebond 57% (7/13)
      · −4.0% : fill 26% (7/30) · rebond 58% (3/7)
      · −5.0% : fill 10% (4/30) · rebond 100% (4/4)
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
- **P(clôture VERTE) selon le drive 15min** (n=140) : 39% en base · 63% si les 15 1res min sont vertes (48 cas) · 25% si rouges (92 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=140) : COUDE à **33min** → P(séance verte=clôture>ouverture) 68% si début vert vs 23% si rouge (base 39% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=49) : tient le vert **68%** · continue >prix actuel 40% ; creux résiduel méd -1.35% (q20 -2.69%) → **SL/trailing à −2.69%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.26% / q75 +2.19% → **scale +1.26% / runner +2.19%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **23%** (continue à baisser 53%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.27%** (au-delà de la MAE q10 -3.27%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-3.03% .. +3.25%] · haut q95 +3.64% · bas q05 -3.54%
   - 60min (n=140) : retour [-3.55% .. +3.01%] · haut q95 +3.9% · bas q05 -3.85%
   - 2h (n=140) : retour [-4.39% .. +3.77%] · haut q95 +4.44% · bas q05 -4.82%
   - 4h (n=140) : retour [-5.27% .. +4.32%] · haut q95 +5.18% · bas q05 -5.48%
   - 6h (n=140) : retour [-5.25% .. +4.81%] · haut q95 +5.93% · bas q05 -6.09%
   - session (n=140) : retour [-4.9% .. +4.25%] · haut q95 +5.95% · bas q05 -6.09%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.03%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 62.8  _(momentum haussier)_
- **ADX** : 12.1  _(pas de tendance nette)_
- **MACD** : hist 15358.375  _(bullish_recent)_
- **BB** : %B 1.18 · largeur 14.7%
- **ATR** : 74714.29 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.103  _(accumulation)_
- **Vol ratio** : 1.66  _(volume au-dessus de la moyenne)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 1403650.0 · MA50 1374760.0 · MA200 1611682.55  _(prix > MA20)_
- **Dist MA** : MA20 +10.1% · MA50 +12.4% · MA200 -4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (82628 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
