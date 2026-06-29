# EVT

**Generated** : 2026-06-29T21:39:00.710829+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €4.97  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €4.97 (+0.4% vs entrée) · entrée €4.95 · stop €4.78 · T1 €5.02 · R/R 0.41  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.043 _(réel 5 s)_ (GBM 0.014) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -360 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.94–€4.97 (mid €4.95)
- Spot actuel : €4.97 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €4.78 (stop swing_plan-based (-2.04%))
- Targets : T1 €5.02 · R/R 0.41 | T2 €5.09 · R/R 0.82 | T3 €5.16 · R/R 1.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.78


## Edge, scénarios & sizing

- EV/risk : 0.014 | EV/share : €0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 61 % | T2 32 % | T3 19 %
- Kelly (position) : f* 0.08 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.8 | bear 6.1 | side 82.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 283.0 (= 57 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.3% → cible +1.367% / stop −3.501%, p_fill 85%, n_eff≈37.0) : P(cible|rempli) **48%** · **EV/risk -0.043** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −0.52% → cible +3.055% / stop −1.528%, p_fill 92%, n_eff≈36.4) : P(cible|rempli) **33%** · **EV/risk -0.083** (×p_fill ; si rempli -0.14% du capital)
  - **deep** (entrée dip −0.766% → cible +4.322% / stop −2.16%, p_fill 90%, n_eff≈35.0) : P(cible|rempli) **28%** · **EV/risk -0.200** (×p_fill ; si rempli -0.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→70% · +2.0%→44% · +3.0%→28% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.63% (p90 7.61%) · excursion haute méd. +1.87% / basse méd. −2.28%
- Profil de vol intra : ouverture 2.984% vs midi 1.271% vs clôture 1.264% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.097 ; mean-reverting — autocorr -0.114)_ ; drift intra méd. 0.256% ; recovery-V 45%
- **σ réalisé intraday** 3.062% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 67% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 4.8351 (VA 4.8161–4.8655 ; dernier close 4.922)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 34% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. -0.03% · baisse 51% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.24%) · haut méd +0.49% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.81% (p90 −2.55%) · haut méd +0.84% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −0.95% (p90 −2.75%) · haut méd +0.95% · range méd 2.08%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −2.96%) · haut méd +0.96% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 4.922 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 85% (130/159) · gap 34% · délai 0.3min · rebond 63% (85/130) (MFE +1.43%)
   - −1.0% : fill 30min 53% · séance 76% (118/159) · gap 21% · délai 1.0min · rebond 65% (75/118) (MFE +1.51%)
   - −1.5% : fill 30min 37% · séance 61% (95/159) · gap 16% · délai 2.6min · rebond 62% (60/95) (MFE +1.35%)
   - −2.0% : fill 30min 31% · séance 50% (77/159) · gap 12% · délai 9.2min · rebond 61% (50/77) (MFE +1.38%)
   - −3.0% : fill 30min 16% · séance 34% (54/159) · gap 6% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 8% · séance 19% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 9% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.43%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.41% (p90 −2.34%) → stop au-delà de −1.11% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.76%) → stop au-delà de −0.99% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=790 jambes) : jambe baissière méd −1.07% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 93% (60/63) · rebond 63% (35/60)
      · −2.0% : fill 70% (45/63) · rebond 64% (29/45)
      · −3.0% : fill 49% (34/63) · rebond 76% (26/34)
      · −4.0% : fill 32% (21/63) · rebond 65% (15/21)
      · −5.0% : fill 18% (14/63) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 81% (28/39) · rebond 78% (22/28)
      · −2.0% : fill 49% (15/39) · rebond 57% (10/15)
      · −3.0% : fill 25% (8/39) · rebond 94% (7/8)
      · −4.0% : fill 12% (3/39) · rebond 52% (1/3)
      · −5.0% : fill 6% (2/39) · rebond 72% (1/2)
   - **gap-up** (57 séances) :
      · −1.0% : fill 54% (30/57) · rebond 56% (18/30)
      · −2.0% : fill 29% (17/57) · rebond 60% (11/17)
      · −3.0% : fill 21% (12/57) · rebond 57% (9/12)
      · −4.0% : fill 9% (5/57) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 66% si les 15 1res min sont vertes (77 cas) · 47% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:07** → P(séance verte=clôture>ouverture) 77% si début vert vs 34% si rouge (base 56% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **77%** · continue >prix actuel 58% ; creux résiduel méd -1.54% (q20 -2.31%) → **SL/trailing à −2.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +2.89% → **scale +1.32% / runner +2.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **34%** (continue à baisser 47%) → **RÉDUIRE ~66%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.71%** (au-delà de la MAE q10 -3.71%), cible rebond +1.63% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.41% .. +2.5%] · haut q95 +3.81% · bas q05 -2.93%
   - 60min (n=160) : retour [-2.82% .. +3.32%] · haut q95 +4.49% · bas q05 -3.35%
   - 2h (n=160) : retour [-3.11% .. +3.23%] · haut q95 +4.63% · bas q05 -3.95%
   - 4h (n=160) : retour [-3.19% .. +3.23%] · haut q95 +4.63% · bas q05 -4.16%
   - 6h (n=160) : retour [-3.57% .. +3.29%] · haut q95 +5.11% · bas q05 -4.45%
   - session (n=160) : retour [-4.42% .. +4.15%] · haut q95 +6.22% · bas q05 -5.36%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.23 · part idiosyncratique 0.77
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 58.5  _(momentum haussier)_
- **ADX** : 12.2  _(pas de tendance nette)_
- **MACD** : hist 0.032  _(bullish_recent)_
- **BB** : %B 0.73 · largeur 13.8%
- **ATR** : 0.18 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.105  _(accumulation)_
- **Vol ratio** : 0.88  _(volume normal)_
- **Choppiness** : 64.0  _(marche en range (choppy))_
- **MA** : MA20 4.81 · MA50 5.01 · MA200 5.56  _(prix > MA20)_
- **Dist MA** : MA20 +3.2% · MA50 -0.9% · MA200 -10.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (96571 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
