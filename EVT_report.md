# EVT

**Generated** : 2026-07-06T21:38:38.570411+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €5.15  

> 🟡 **WAIT-FOR-DIP** — spot +2.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €5.15 (+2.4% vs entrée) · entrée €5.03 · stop €4.96 · T1 €5.16 · R/R 1.86  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.205 _(réel 5 s)_ (GBM 0.12) · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 239 % hors [0,100] (R² max 0.56). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €5.00–€5.06 (mid €5.03)
- Spot actuel : €5.15 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : €4.96 (stop swing_plan-based (-3.66%))
- Targets : T1 €5.16 · R/R 1.86 | T2 €5.30 · R/R 3.86 | T3 €5.43 · R/R 5.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.96


## Edge, scénarios & sizing

- EV/risk : 0.12 | EV/share : €0.008 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 25 % | T3 16 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 17.6 | bear 6.4 | side 76.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 397.0 (= 77 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.068% → cible +1.191% / stop −3.5%, p_fill 63%, n_eff≈28.8) : P(cible|rempli) **72%** · **EV/risk +0.046** (×p_fill ; si rempli +0.26% du capital)
  - **swing** (entrée dip −2.359% → cible +2.663% / stop −1.332%, p_fill 50%, n_eff≈24.7) : P(cible|rempli) **50%** · **EV/risk +0.205** (×p_fill ; si rempli +0.55% du capital)
  - **deep** (entrée dip −3.646% → cible +3.766% / stop −1.882%, p_fill 53%, n_eff≈22.4) : P(cible|rempli) **21%** · **EV/risk -0.224** (×p_fill ; si rempli -0.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→48% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.47% (p90 6.71%) · excursion haute méd. +1.98% / basse méd. −1.94%
- Profil de vol intra : ouverture 2.715% vs midi 1.233% vs clôture 1.244% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 43%)_
- **Régime intraday** : **chop** _(efficiency 0.084 ; mean-reverting — autocorr -0.124)_ ; drift intra méd. 0.429% ; recovery-V 53%
- **σ réalisé intraday** 3.006% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 62% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 5.1569 (VA 5.1341–5.2284 ; dernier close 5.18)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 31% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. -0.02% · baisse 50% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.6% (p90 −2.15%) · haut méd +0.75% · range méd 1.45%
- Excursion ouverture 15min (n=160) : bas méd −0.79% (p90 −2.37%) · haut méd +0.88% · range méd 1.77%
- Excursion ouverture 30min (n=160) : bas méd −0.88% (p90 −2.73%) · haut méd +0.97% · range méd 2.2%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.92%) · haut méd +0.97% · range méd 2.38%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 5.18 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 83% (131/159) · gap 33% · délai 0.3min · rebond 64% (86/131) (MFE +1.48%)
   - −1.0% : fill 30min 52% · séance 75% (119/159) · gap 21% · délai 1.0min · rebond 67% (77/119) (MFE +1.56%)
   - −1.5% : fill 30min 34% · séance 56% (94/159) · gap 15% · délai 2.5min · rebond 62% (59/94) (MFE +1.35%)
   - −2.0% : fill 30min 28% · séance 46% (76/159) · gap 11% · délai 9.2min · rebond 61% (49/76) (MFE +1.37%)
   - −3.0% : fill 30min 15% · séance 31% (54/159) · gap 5% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 7% · séance 18% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.39% (p90 −2.18%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.43% (p90 −2.03%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.4% (p90 −1.73%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=786 jambes) : jambe baissière méd −1.06% (p90 −2.33%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (63 séances) :
      · −1.0% : fill 94% (60/63) · rebond 65% (35/60)
      · −2.0% : fill 67% (44/63) · rebond 63% (28/44)
      · −3.0% : fill 47% (34/63) · rebond 76% (26/34)
      · −4.0% : fill 31% (21/63) · rebond 65% (15/21)
      · −5.0% : fill 17% (14/63) · rebond 74% (10/14)
   - **flat** (40 séances) :
      · −1.0% : fill 84% (30/40) · rebond 82% (24/30)
      · −2.0% : fill 42% (15/40) · rebond 57% (10/15)
      · −3.0% : fill 21% (8/40) · rebond 94% (7/8)
      · −4.0% : fill 11% (3/40) · rebond 52% (1/3)
      · −5.0% : fill 5% (2/40) · rebond 72% (1/2)
   - **gap-up** (56 séances) :
      · −1.0% : fill 49% (29/56) · rebond 56% (18/29)
      · −2.0% : fill 26% (17/56) · rebond 60% (11/17)
      · −3.0% : fill 19% (12/56) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/56) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/56) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 60% en base · 71% si les 15 1res min sont vertes (79 cas) · 49% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:05** → P(séance verte=clôture>ouverture) 80% si début vert vs 37% si rouge (base 60% · écart 43 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **80%** · continue >prix actuel 57% ; creux résiduel méd -1.49% (q20 -2.45%) → **SL/trailing à −2.45%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.44% → **scale +1.18% / runner +2.44%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **37%** (continue à baisser 44%) → **RÉDUIRE ~63%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.72%** (au-delà de la MAE q10 -3.72%), cible rebond +1.57% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.38% .. +2.44%] · haut q95 +3.63% · bas q05 -2.88%
   - 60min (n=160) : retour [-2.79% .. +3.14%] · haut q95 +4.37% · bas q05 -3.34%
   - 2h (n=160) : retour [-3.02% .. +3.21%] · haut q95 +4.55% · bas q05 -3.93%
   - 4h (n=160) : retour [-2.96% .. +3.03%] · haut q95 +4.55% · bas q05 -3.96%
   - 6h (n=160) : retour [-3.36% .. +3.26%] · haut q95 +4.77% · bas q05 -4.33%
   - session (n=160) : retour [-4.27% .. +4.1%] · haut q95 +5.93% · bas q05 -5.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 76.7  _(surachat)_
- **ADX** : 19.2  _(pas de tendance nette)_
- **MACD** : hist 0.056  _(pas de croisement recent)_
- **BB** : %B 0.91 · largeur 16.1%
- **ATR** : 0.18 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.116  _(accumulation)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 47.1  _(transition)_
- **MA** : MA20 4.83 · MA50 4.97 · MA200 5.54  _(prix > MA20)_
- **Dist MA** : MA20 +6.5% · MA50 +3.6% · MA200 -7.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93511 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
