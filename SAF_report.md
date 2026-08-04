# SAF

**Generated** : 2026-08-04T00:06:51.290751+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €350.70  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €350.70 (+0.4% vs entrée) · entrée €349.33 · stop €339.76 · T1 €357.72 · R/R 0.88  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.089 _(réel 5 s)_ (GBM 0.007) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 187 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 8/10 élevée alors que : %B 1.03 (collé à la bande haute) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €347.96–€350.70 (mid €349.33)
- Spot actuel : €350.70 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €339.76 (stop swing_plan-based (-3.12%))
- Targets : T1 €357.72 · R/R 0.88 | T2 €366.10 · R/R 1.75 | T3 €374.49 · R/R 2.63
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €339.76


## Edge, scénarios & sizing

- EV/risk : 0.007 | EV/share : €0.068 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 23 % | T3 14 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 37.4 | side 57.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 351.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.296% → cible +1.073% / stop −2.0%, p_fill 84%, n_eff≈33.1) : P(cible|rempli) **35%** · **EV/risk -0.103** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −0.391% → cible +2.4% / stop −2.74%, p_fill 85%, n_eff≈32.4) : P(cible|rempli) **48%** · **EV/risk -0.089** (×p_fill ; si rempli -0.29% du capital)
  - **deep** (entrée dip −0.486% → cible +3.394% / stop −4.114%, p_fill 83%, n_eff≈31.5) : P(cible|rempli) **59%** · **EV/risk +0.028** (×p_fill ; si rempli +0.14% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→71% · +1.0%→54% · +2.0%→32% · +3.0%→14% · +5.0%→2% · +8.0%→1%
- Range intraday médian 2.7% (p90 4.55%) · excursion haute méd. +1.13% / basse méd. −1.01%
- Profil de vol intra : ouverture 1.664% vs midi 0.63% vs clôture 0.744% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 41% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.095 ; mean-reverting — autocorr -0.046)_ ; drift intra méd. 0.035% ; recovery-V 23%
- **σ réalisé intraday** 1.96% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 50% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 339.9431 (VA 337.7019–344.0181 ; dernier close 339.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 18% · rebond 54% · **stop −1.63%** sous le fill (sous le bruit) · cible +1.2% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. 0.02% · baisse 49% (gap-down >1% 9% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.5% (p90 −1.72%) · haut méd +0.18% · range méd 0.94%
- Excursion ouverture 15min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.3% · range méd 1.2%
- Excursion ouverture 30min (n=160) : bas méd −0.62% (p90 −1.92%) · haut méd +0.52% · range méd 1.42%
- Excursion ouverture 60min (n=160) : bas méd −0.73% (p90 −1.96%) · haut méd +0.58% · range méd 1.6%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 339.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 70% (114/159) · gap 22% · délai 0.2min · rebond 42% (44/114) (MFE +0.84%)
   - −1.0% : fill 30min 43% · séance 54% (83/159) · gap 9% · délai 0.4min · rebond 43% (31/83) (MFE +0.67%)
   - −1.5% : fill 30min 29% · séance 44% (70/159) · gap 3% · délai 7.5min · rebond 45% (26/70) (MFE +0.91%)
   - −2.0% : fill 30min 14% · séance 34% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 18% (29/159) · gap 1% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 8% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −0.91%) → stop au-delà de −0.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.16% (p90 −0.83%) → stop au-delà de −0.64% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=207 jambes) : jambe baissière méd −1.09% (p90 −2.48%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 82% (44/55) · rebond 37% (16/44)
      · −2.0% : fill 63% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 30% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 16% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (45 séances) :
      · −1.0% : fill 45% (19/45) · rebond 56% (10/19)
      · −2.0% : fill 21% (9/45) · rebond 75% (5/9)
      · −3.0% : fill 11% (5/45) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/45) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/45) · rebond 0% (0/0)
   - **gap-up** (59 séances) :
      · −1.0% : fill 34% (20/59) · rebond 42% (5/20)
      · −2.0% : fill 18% (11/59) · rebond 43% (4/11)
      · −3.0% : fill 11% (7/59) · rebond 36% (4/7)
      · −4.0% : fill 5% (3/59) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/59) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 69% si les 15 1res min sont vertes (70 cas) · 33% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 77% si début vert vs 26% si rouge (base 50% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 298min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **77%** · continue >prix actuel 59% ; creux résiduel méd -0.59% (q20 -1.61%) → **SL/trailing à −1.61%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.26% / q75 +1.76% → **scale +1.26% / runner +1.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **26%** (continue à baisser 47%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.43%** (au-delà de la MAE q10 -2.43%), cible rebond +1.05% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.62% .. +1.56%] · haut q95 +1.96% · bas q05 -2.28%
   - 60min (n=160) : retour [-1.82% .. +2.1%] · haut q95 +2.13% · bas q05 -2.58%
   - 2h (n=160) : retour [-2.45% .. +2.14%] · haut q95 +2.54% · bas q05 -3.06%
   - 4h (n=160) : retour [-2.13% .. +2.18%] · haut q95 +2.98% · bas q05 -3.38%
   - 6h (n=160) : retour [-2.23% .. +2.83%] · haut q95 +3.22% · bas q05 -3.94%
   - session (n=160) : retour [-3.29% .. +2.71%] · haut q95 +3.64% · bas q05 -4.06%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 69.3  _(momentum haussier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist 1.006  _(bullish_recent)_
- **BB** : %B 1.03 · largeur 9.6%
- **ATR** : 9.57 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.059  _(accumulation)_
- **Vol ratio** : 0.37  _(volume atone)_
- **Choppiness** : 49.6  _(transition)_
- **MA** : MA20 333.78 · MA50 325.04 · MA200 305.57  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 +7.9% · MA200 +14.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93566 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
