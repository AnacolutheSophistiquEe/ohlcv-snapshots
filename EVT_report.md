# EVT

**Generated** : 2026-07-03T21:38:50.409175+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €5.14  

> 🟡 **WAIT-FOR-DIP** — spot +1.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €5.14 (+1.0% vs entrée) · entrée €5.09 · stop €4.91 · T1 €5.15 · R/R 0.33  
> ↳ P(T1 av. stop) 69 % _(réel 5 s)_ · EV/risk 0.044 _(réel 5 s)_ (GBM 0.051) · ¼-Kelly 0.037 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -295 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €5.07–€5.10 (mid €5.09)
- Spot actuel : €5.14 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : €4.91 (stop swing_plan-based (-6.4%))
- Targets : T1 €5.15 · R/R 0.33 | T2 €5.22 · R/R 0.72 | T3 €5.29 · R/R 1.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.91


## Edge, scénarios & sizing

- EV/risk : 0.051 | EV/share : €0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 66 % | T2 34 % | T3 21 %
- Kelly (position) : f* 0.149 | ¼-Kelly 0.037 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.9 | bear 6.2 | side 81.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 288.0 (= 56 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.025% → cible +1.319% / stop −3.501%, p_fill 62%, n_eff≈29.4) : P(cible|rempli) **69%** · **EV/risk +0.044** (×p_fill ; si rempli +0.25% du capital)
  - **swing** (entrée dip −2.25% → cible +8.487% / stop −4.246%, p_fill 52%, n_eff≈24.8) : P(cible|rempli) **33%** · **EV/risk +0.034** (×p_fill ; si rempli +0.28% du capital)
  - **deep** (entrée dip −3.488% → cible +4.171% / stop −2.084%, p_fill 57%, n_eff≈23.6) : P(cible|rempli) **24%** · **EV/risk -0.193** (×p_fill ; si rempli -0.70% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→72% · +2.0%→48% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.5% (p90 6.99%) · excursion haute méd. +1.98% / basse méd. −2.02%
- Profil de vol intra : ouverture 2.773% vs midi 1.236% vs clôture 1.247% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.087 ; mean-reverting — autocorr -0.114)_ ; drift intra méd. 0.426% ; recovery-V 49%
- **σ réalisé intraday** 3.041% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 74% / bas 60% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 5.1073 (VA 5.1073–5.2039 ; dernier close 5.174)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 31% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 49% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.61% (p90 −2.17%) · haut méd +0.64% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.41%) · haut méd +0.85% · range méd 1.78%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.74%) · haut méd +0.96% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.01% (p90 −2.93%) · haut méd +0.97% · range méd 2.39%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 5.174 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 82% (130/159) · gap 33% · délai 0.3min · rebond 65% (86/130) (MFE +1.49%)
   - −1.0% : fill 30min 53% · séance 75% (118/159) · gap 22% · délai 1.0min · rebond 67% (76/118) (MFE +1.68%)
   - −1.5% : fill 30min 35% · séance 57% (94/159) · gap 15% · délai 2.5min · rebond 62% (59/94) (MFE +1.35%)
   - −2.0% : fill 30min 29% · séance 47% (76/159) · gap 12% · délai 9.2min · rebond 61% (49/76) (MFE +1.37%)
   - −3.0% : fill 30min 15% · séance 31% (54/159) · gap 5% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 7% · séance 18% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 3% · séance 9% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.19%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.42% (p90 −2.02%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.73%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=792 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 94% (60/63) · rebond 65% (35/60)
      · −2.0% : fill 67% (44/63) · rebond 63% (28/44)
      · −3.0% : fill 47% (34/63) · rebond 76% (26/34)
      · −4.0% : fill 31% (21/63) · rebond 65% (15/21)
      · −5.0% : fill 17% (14/63) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 83% (29/39) · rebond 80% (23/29)
      · −2.0% : fill 45% (15/39) · rebond 57% (10/15)
      · −3.0% : fill 23% (8/39) · rebond 94% (7/8)
      · −4.0% : fill 11% (3/39) · rebond 52% (1/3)
      · −5.0% : fill 6% (2/39) · rebond 72% (1/2)
   - **gap-up** (57 séances) :
      · −1.0% : fill 49% (29/57) · rebond 56% (18/29)
      · −2.0% : fill 26% (17/57) · rebond 60% (11/17)
      · −3.0% : fill 19% (12/57) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/57) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/57) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 60% en base · 70% si les 15 1res min sont vertes (79 cas) · 49% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:07** → P(séance verte=clôture>ouverture) 79% si début vert vs 36% si rouge (base 60% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **79%** · continue >prix actuel 56% ; creux résiduel méd -1.57% (q20 -2.68%) → **SL/trailing à −2.68%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.51% → **scale +1.13% / runner +2.51%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **36%** (continue à baisser 45%) → **RÉDUIRE ~64%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.6%** (au-delà de la MAE q10 -3.6%), cible rebond +1.66% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.38% .. +2.44%] · haut q95 +3.68% · bas q05 -2.89%
   - 60min (n=160) : retour [-2.79% .. +3.18%] · haut q95 +4.4% · bas q05 -3.34%
   - 2h (n=160) : retour [-3.03% .. +3.21%] · haut q95 +4.57% · bas q05 -3.93%
   - 4h (n=160) : retour [-2.96% .. +3.06%] · haut q95 +4.57% · bas q05 -4.0%
   - 6h (n=160) : retour [-3.38% .. +3.26%] · haut q95 +4.84% · bas q05 -4.34%
   - session (n=160) : retour [-4.3% .. +4.11%] · haut q95 +5.99% · bas q05 -5.33%


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 69.6  _(momentum haussier)_
- **ADX** : 14.9  _(pas de tendance nette)_
- **MACD** : hist 0.052  _(pas de croisement recent)_
- **BB** : %B 0.98 · largeur 14.0%
- **ATR** : 0.18 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.149  _(accumulation)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 49.6  _(transition)_
- **MA** : MA20 4.81 · MA50 4.99 · MA200 5.55  _(prix > MA20)_
- **Dist MA** : MA20 +6.8% · MA50 +2.9% · MA200 -7.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (95622 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
