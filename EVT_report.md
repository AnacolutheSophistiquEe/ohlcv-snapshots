# EVT

**Generated** : 2026-07-09T00:04:38.074983+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €4.86  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €4.86 (+4.5% vs entrée) · entrée €4.65 · stop €4.59 · T1 €4.76 · R/R 1.83  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.129 · ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -72 % hors [0,100] (R² max 0.56). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €4.62–€4.67 (mid €4.65)
- Spot actuel : €4.86 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : €4.59 (stop swing_plan-based (-5.55%))
- Targets : T1 €4.76 · R/R 1.83 | T2 €4.88 · R/R 3.83 | T3 €5.00 · R/R 5.83
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.59


## Edge, scénarios & sizing

- EV/risk : 0.129 | EV/share : €0.008 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 25 % | T3 17 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.5 | bear 6.3 | side 74.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 286.0 (= 59 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.969% → cible +1.139% / stop −3.5%, p_fill 36%, n_eff≈18.6) : P(cible|rempli) **54%** · **EV/risk +0.015** (×p_fill ; si rempli +0.15% du capital)
  - **swing** (entrée dip −4.321% → cible +2.546% / stop −1.274%, p_fill 17%, n_eff≈10.9) : P(cible|rempli) **11%** · **EV/risk -0.119** (×p_fill ; si rempli -0.90% du capital)
  - **deep** (entrée dip −6.69% → cible +3.599% / stop −1.801%, p_fill 29%, n_eff≈12.8) : P(cible|rempli) **56%** · **EV/risk +0.173** (×p_fill ; si rempli +1.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→46% · +3.0%→29% · +5.0%→9% · +8.0%→2%
- Range intraday médian 4.4% (p90 6.71%) · excursion haute méd. +1.92% / basse méd. −1.83%
- Profil de vol intra : ouverture 2.663% vs midi 1.233% vs clôture 1.242% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 42%)_
- **Régime intraday** : **chop** _(efficiency 0.082 ; mean-reverting — autocorr -0.124)_ ; drift intra méd. 0.323% ; recovery-V 49%
- **σ réalisé intraday** 2.945% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 65% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 5.1293 (VA 5.1103–5.1901 ; dernier close 5.04)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 30% · rebond 75% · **stop −2.37%** sous le fill (sous le bruit) · cible +2.14% · R/R 0.9 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.57% (p90 −2.11%) · haut méd +0.77% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.29%) · haut méd +0.88% · range méd 1.76%
- Excursion ouverture 30min (n=160) : bas méd −0.82% (p90 −2.72%) · haut méd +1.03% · range méd 2.09%
- Excursion ouverture 60min (n=160) : bas méd −0.89% (p90 −2.86%) · haut méd +1.05% · range méd 2.33%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 5.04 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 84% (133/159) · gap 33% · délai 0.3min · rebond 65% (88/133) (MFE +1.39%)
   - −1.0% : fill 30min 50% · séance 76% (121/159) · gap 20% · délai 1.3min · rebond 69% (79/121) (MFE +1.56%)
   - −1.5% : fill 30min 33% · séance 57% (96/159) · gap 14% · délai 15.1min · rebond 64% (61/96) (MFE +1.47%)
   - −2.0% : fill 30min 27% · séance 46% (77/159) · gap 11% · délai 14.4min · rebond 63% (50/77) (MFE +1.44%)
   - −3.0% : fill 30min 14% · séance 30% (54/159) · gap 5% · délai 30.7min · rebond 75% (42/54) (MFE +2.14%)
   - −4.0% : fill 30min 7% · séance 17% (29/159) · gap 1% · délai 46.2min · rebond 66% (19/29) (MFE +1.67%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 0% · délai 63.2min · rebond 75% (12/17) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −2.12%) → stop au-delà de −1.48% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.42% (p90 −2.03%) → stop au-delà de −1.22% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.73%) → stop au-delà de −0.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=787 jambes) : jambe baissière méd −1.05% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 94% (62/65) · rebond 68% (37/62)
      · −2.0% : fill 66% (45/65) · rebond 66% (29/45)
      · −3.0% : fill 43% (34/65) · rebond 76% (26/34)
      · −4.0% : fill 28% (21/65) · rebond 65% (15/21)
      · −5.0% : fill 16% (14/65) · rebond 74% (10/14)
   - **flat** (39 séances) :
      · −1.0% : fill 85% (30/39) · rebond 82% (24/30)
      · −2.0% : fill 42% (15/39) · rebond 57% (10/15)
      · −3.0% : fill 21% (8/39) · rebond 94% (7/8)
      · −4.0% : fill 11% (3/39) · rebond 52% (1/3)
      · −5.0% : fill 5% (2/39) · rebond 72% (1/2)
   - **gap-up** (55 séances) :
      · −1.0% : fill 49% (29/55) · rebond 56% (18/29)
      · −2.0% : fill 26% (17/55) · rebond 60% (11/17)
      · −3.0% : fill 19% (12/55) · rebond 57% (9/12)
      · −4.0% : fill 8% (5/55) · rebond 80% (3/5)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 60% en base · 69% si les 15 1res min sont vertes (80 cas) · 49% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:05** → P(séance verte=clôture>ouverture) 81% si début vert vs 36% si rouge (base 60% · écart 45 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **81%** · continue >prix actuel 58% ; creux résiduel méd -1.45% (q20 -2.32%) → **SL/trailing à −2.32%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.17% / q75 +2.38% → **scale +1.17% / runner +2.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **36%** (continue à baisser 46%) → **RÉDUIRE ~64%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.72%** (au-delà de la MAE q10 -3.72%), cible rebond +1.53% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.37% .. +2.43%] · haut q95 +3.55% · bas q05 -2.86%
   - 60min (n=160) : retour [-2.77% .. +3.05%] · haut q95 +4.32% · bas q05 -3.32%
   - 2h (n=160) : retour [-3.0% .. +3.2%] · haut q95 +4.51% · bas q05 -3.77%
   - 4h (n=160) : retour [-2.95% .. +3.0%] · haut q95 +4.51% · bas q05 -3.93%
   - 6h (n=160) : retour [-3.35% .. +3.24%] · haut q95 +4.64% · bas q05 -4.32%
   - session (n=160) : retour [-4.2% .. +4.07%] · haut q95 +5.7% · bas q05 -5.31%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.89%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.4  _(momentum haussier)_
- **ADX** : 18.6  _(pas de tendance nette)_
- **MACD** : hist 0.025  _(pas de croisement recent)_
- **BB** : %B 0.49 · largeur 15.5%
- **ATR** : 0.17 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.152  _(accumulation)_
- **Vol ratio** : 0.39  _(volume atone)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 4.86 · MA50 4.96 · MA200 5.52  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 -2.1% · MA200 -12.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93552 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
