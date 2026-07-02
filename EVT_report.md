# EVT

**Generated** : 2026-07-02T21:39:02.579684+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €5.14  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €5.14 (+2.2% vs entrée) · entrée €5.03 · stop €4.81 · T1 €5.45 · R/R 1.91  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk 0.036 _(réel 5 s)_ (GBM -0.035) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -300 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €5.00–€5.06 (mid €5.03)
- Spot actuel : €5.14 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €4.81 (stop swing_plan-based (-6.43%))
- Targets : T1 €5.45 · R/R 1.91 | T2 €5.46 · R/R 1.95 | T3 €5.47 · R/R 2.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.81


## Edge, scénarios & sizing

- EV/risk : -0.035 | EV/share : €-0.007 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 17 % | T3 17 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 17.3 | bear 6.4 | side 76.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 283.0 (= 55 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.048% → cible +1.322% / stop −3.498%, p_fill 60%, n_eff≈30.2) : P(cible|rempli) **67%** · **EV/risk +0.031** (×p_fill ; si rempli +0.18% du capital)
  - **swing** (entrée dip −2.308% → cible +8.44% / stop −4.22%, p_fill 55%, n_eff≈25.0) : P(cible|rempli) **33%** · **EV/risk +0.036** (×p_fill ; si rempli +0.28% du capital)
  - **deep** (entrée dip −3.564% → cible +4.18% / stop −2.09%, p_fill 60%, n_eff≈23.7) : P(cible|rempli) **24%** · **EV/risk -0.199** (×p_fill ; si rempli -0.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→71% · +2.0%→46% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.52% (p90 6.99%) · excursion haute méd. +1.93% / basse méd. −2.1%
- Profil de vol intra : ouverture 2.799% vs midi 1.236% vs clôture 1.253% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.089 ; mean-reverting — autocorr -0.114)_ ; drift intra méd. 0.383% ; recovery-V 45%
- **σ réalisé intraday** 3.063% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 72% / bas 63% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 5.1594 (VA 5.1085–5.1933 ; dernier close 5.11)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 32% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. -0.02% · baisse 50% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.59% (p90 −2.19%) · haut méd +0.62% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.45%) · haut méd +0.89% · range méd 1.8%
- Excursion ouverture 30min (n=160) : bas méd −0.87% (p90 −2.74%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.93%) · haut méd +0.97% · range méd 2.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 5.11 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 82% (129/159) · gap 34% · délai 0.2min · rebond 64% (85/129) (MFE +1.48%)
   - −1.0% : fill 30min 52% · séance 74% (117/159) · gap 22% · délai 0.9min · rebond 66% (75/117) (MFE +1.56%)
   - −1.5% : fill 30min 35% · séance 58% (94/159) · gap 16% · délai 2.5min · rebond 62% (59/94) (MFE +1.35%)
   - −2.0% : fill 30min 29% · séance 48% (76/159) · gap 12% · délai 9.2min · rebond 61% (49/76) (MFE +1.37%)
   - −3.0% : fill 30min 15% · séance 32% (54/159) · gap 5% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 7% · séance 18% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 9% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −2.24%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.37% (p90 −2.13%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.73%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=794 jambes) : jambe baissière méd −1.07% (p90 −2.34%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 94% (60/63) · rebond 65% (35/60)
      · −2.0% : fill 67% (44/63) · rebond 63% (28/44)
      · −3.0% : fill 47% (34/63) · rebond 76% (26/34)
      · −4.0% : fill 31% (21/63) · rebond 65% (15/21)
      · −5.0% : fill 17% (14/63) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 81% (28/39) · rebond 78% (22/28)
      · −2.0% : fill 49% (15/39) · rebond 57% (10/15)
      · −3.0% : fill 25% (8/39) · rebond 94% (7/8)
      · −4.0% : fill 12% (3/39) · rebond 52% (1/3)
      · −5.0% : fill 6% (2/39) · rebond 72% (1/2)
   - **gap-up** (57 séances) :
      · −1.0% : fill 49% (29/57) · rebond 56% (18/29)
      · −2.0% : fill 26% (17/57) · rebond 60% (11/17)
      · −3.0% : fill 19% (12/57) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/57) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 59% en base · 70% si les 15 1res min sont vertes (79 cas) · 47% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:07** → P(séance verte=clôture>ouverture) 79% si début vert vs 34% si rouge (base 59% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -1.57% (q20 -2.71%) → **SL/trailing à −2.71%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.12% / q75 +2.5% → **scale +1.12% / runner +2.5%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **34%** (continue à baisser 47%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.71%** (au-delà de la MAE q10 -3.71%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.39% .. +2.45%] · haut q95 +3.73% · bas q05 -2.9%
   - 60min (n=160) : retour [-2.8% .. +3.22%] · haut q95 +4.42% · bas q05 -3.34%
   - 2h (n=160) : retour [-3.05% .. +3.22%] · haut q95 +4.59% · bas q05 -3.94%
   - 4h (n=160) : retour [-3.02% .. +3.1%] · haut q95 +4.59% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.43% .. +3.27%] · haut q95 +4.91% · bas q05 -4.37%
   - session (n=160) : retour [-4.33% .. +4.12%] · haut q95 +6.05% · bas q05 -5.33%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.91%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.23 · part idiosyncratique 0.77
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 69.7  _(momentum haussier)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist 0.052  _(pas de croisement recent)_
- **BB** : %B 0.99 · largeur 14.1%
- **ATR** : 0.18 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.164  _(accumulation)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 49.2  _(transition)_
- **MA** : MA20 4.81 · MA50 4.99 · MA200 5.55  _(prix > MA20)_
- **Dist MA** : MA20 +6.9% · MA50 +3.0% · MA200 -7.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (95866 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
