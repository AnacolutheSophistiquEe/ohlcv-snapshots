# SAF

**Generated** : 2026-07-21T00:06:48.210520+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €325.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot €325.60 (+2.6% vs entrée) · entrée €317.21 · stop €310.86 · T1 €320.50 · R/R 0.52  
> ↳ P(T1 av. stop) 57 % · EV/risk 0.049 · ¼-Kelly 0.023 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €316.55–€317.87 (mid €317.21)
- Spot actuel : €325.60 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €310.86 (stop swing_plan-based (-6.77%))
- Targets : T1 €320.50 · R/R 0.52 | T2 €323.80 · R/R 1.04 | T3 €327.09 · R/R 1.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €310.86


## Edge, scénarios & sizing

- EV/risk : 0.049 | EV/share : €0.312 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 35 % | T3 14 %
- Kelly (position) : f* 0.092 | ¼-Kelly 0.023 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 17.4 | side 77.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=6))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→72% · +1.0%→57% · +2.0%→38% · +3.0%→15% · +5.0%→4% · +8.0%→1%
- Range intraday médian 2.72% (p90 4.55%) · excursion haute méd. +1.52% / basse méd. −0.95%
- Profil de vol intra : ouverture 1.625% vs midi 0.628% vs clôture 0.755% _(ouverture ~2.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 39% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; mean-reverting — autocorr -0.045)_ ; drift intra méd. 0.162% ; recovery-V 36%
- **σ réalisé intraday** 1.789% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 54% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 325.145 (VA 324.465–326.165 ; dernier close 330.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 19% · rebond 49% · **stop −1.79%** sous le fill (sous le bruit) · cible +0.95% · R/R 0.53 (high win-rate)
- Gaps overnight (n=151) : méd. -0.06% · baisse 51% (gap-down >1% 11% · >2% 2%)
- Excursion ouverture 5min (n=152) : bas méd −0.45% (p90 −1.5%) · haut méd +0.21% · range méd 0.92%
- Excursion ouverture 15min (n=152) : bas méd −0.6% (p90 −1.61%) · haut méd +0.36% · range méd 1.18%
- Excursion ouverture 30min (n=152) : bas méd −0.62% (p90 −1.68%) · haut méd +0.47% · range méd 1.28%
- Excursion ouverture 60min (n=152) : bas méd −0.73% (p90 −1.88%) · haut méd +0.57% · range méd 1.5%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 330.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 68% (107/151) · gap 27% · délai 0.2min · rebond 39% (40/107) (MFE +0.78%)
   - −1.0% : fill 30min 44% · séance 55% (79/151) · gap 11% · délai 0.4min · rebond 43% (29/79) (MFE +0.63%)
   - −1.5% : fill 30min 29% · séance 46% (67/151) · gap 4% · délai 15.9min · rebond 40% (23/67) (MFE +0.89%)
   - −2.0% : fill 30min 12% · séance 35% (49/151) · gap 2% · délai 75.5min · rebond 44% (21/49) (MFE +0.78%)
   - −3.0% : fill 30min 4% · séance 19% (28/151) · gap 1% · délai 202.9min · rebond 49% (16/28) (MFE +0.95%)
   - −4.0% : fill 30min 2% · séance 9% (13/151) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/151) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −0.91%) → stop au-delà de −0.76% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.91%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=183 jambes) : jambe baissière méd −1.07% (p90 −2.56%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 81% (43/54) · rebond 39% (16/43)
      · −2.0% : fill 61% (31/54) · rebond 44% (14/31)
      · −3.0% : fill 32% (17/54) · rebond 50% (9/17)
      · −4.0% : fill 17% (9/54) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/54) · rebond 0% (0/2)
   - **flat** (42 séances) :
      · −1.0% : fill 47% (18/42) · rebond 73% (10/18)
      · −2.0% : fill 14% (7/42) · rebond 50% (3/7)
      · −3.0% : fill 7% (4/42) · rebond 69% (3/4)
      · −4.0% : fill 1% (1/42) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/42) · rebond 0% (0/0)
   - **gap-up** (55 séances) :
      · −1.0% : fill 30% (18/55) · rebond 17% (3/18)
      · −2.0% : fill 22% (11/55) · rebond 43% (4/11)
      · −3.0% : fill 14% (7/55) · rebond 36% (4/7)
      · −4.0% : fill 6% (3/55) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/55) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 54% en base · 72% si les 15 1res min sont vertes (67 cas) · 37% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=152) : COUDE à **44min** → P(séance verte=clôture>ouverture) 82% si début vert vs 30% si rouge (base 54% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 297min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=67) : tient le vert **82%** · continue >prix actuel 64% ; creux résiduel méd -0.57% (q20 -1.41%) → **SL/trailing à −1.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.32% / q75 +1.78% → **scale +1.32% / runner +1.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **30%** (continue à baisser 49%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.52%** (au-delà de la MAE q10 -2.52%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-1.59% .. +1.58%] · haut q95 +1.94% · bas q05 -2.22%
   - 60min (n=152) : retour [-1.64% .. +2.14%] · haut q95 +2.68% · bas q05 -2.34%
   - 2h (n=152) : retour [-2.28% .. +2.19%] · haut q95 +2.73% · bas q05 -2.94%
   - 4h (n=152) : retour [-2.21% .. +2.19%] · haut q95 +3.27% · bas q05 -3.06%
   - 6h (n=152) : retour [-2.32% .. +2.96%] · haut q95 +3.45% · bas q05 -3.38%
   - session (n=152) : retour [-3.45% .. +3.28%] · haut q95 +3.68% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 2.0% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.67%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.2  _(momentum baissier)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist -3.732  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 11.8%
- **ATR** : 8.57 (57.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.245  _(accumulation)_
- **Vol ratio** : 0.25  _(volume atone)_
- **Choppiness** : 42.9  _(transition)_
- **MA** : MA20 338.66 · MA50 313.75 · MA200 303.65  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 +3.8% · MA200 +7.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88794 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
