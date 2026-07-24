# RHM

**Generated** : 2026-07-24T21:35:43.633846+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €1037.60  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1037.60 (+2.6% vs entrée) · entrée €1011.33 · stop €991.10 · T1 €1027.21 · R/R 0.78  
> ↳ P(T1 av. stop) 27 % _(réel 5 s)_ · EV/risk -0.122 _(réel 5 s)_ (GBM 0.006) · ¼-Kelly 0.013 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1008.15–€1014.50 (mid €1011.33)
- Spot actuel : €1037.60 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €991.10 (stop swing_plan-based (-7.23%))
- Targets : T1 €1027.21 · R/R 0.78 | T2 €1043.10 · R/R 1.57 | T3 €1058.99 · R/R 2.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €991.10


## Edge, scénarios & sizing

- EV/risk : 0.006 | EV/share : €0.114 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 25 % | T3 3 %
- Kelly (position) : f* 0.05 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 54.1 | bear 5.0 | side 40.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.531% → cible +1.571% / stop −2.0%, p_fill 28%, n_eff≈12.1) : P(cible|rempli) **27%** · **EV/risk -0.122** (×p_fill ; si rempli -0.88% du capital)
  - **swing** (entrée dip −5.571% → cible +3.513% / stop −1.757%, p_fill 26%, n_eff≈10.2) : P(cible|rempli) **27%** · **EV/risk -0.072** (×p_fill ; si rempli -0.48% du capital)
  - **deep** (entrée dip −8.61% → cible +4.968% / stop −2.484%, p_fill 31%, n_eff≈10.0) : P(cible|rempli) **5%** · **EV/risk -0.244** (×p_fill ; si rempli -1.98% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→48% · +3.0%→28% · +5.0%→1% · +8.0%→0%
- Range intraday médian 4.06% (p90 6.65%) · excursion haute méd. +1.85% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.537% vs midi 0.856% vs clôture 1.082% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.1 ; neutre — autocorr -0.011)_ ; drift intra méd. -0.25% ; recovery-V 45%
- **σ réalisé intraday** 2.766% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 73% / bas 66% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 1015.4987 (VA 1009.4787–1019.2613 ; dernier close 1012.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 61% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 44% (gap-down >1% 13% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −1.74%) · haut méd +0.57% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.0%) · haut méd +0.68% · range méd 1.9%
- Excursion ouverture 30min (n=160) : bas méd −1.06% (p90 −2.73%) · haut méd +0.87% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −2.9%) · haut méd +1.0% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1012.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (123/159) · gap 29% · délai 0.3min · rebond 59% (65/123) (MFE +1.34%)
   - −1.0% : fill 30min 50% · séance 70% (110/159) · gap 13% · délai 4.2min · rebond 62% (64/110) (MFE +1.4%)
   - −1.5% : fill 30min 32% · séance 56% (82/159) · gap 7% · délai 17.8min · rebond 51% (42/82) (MFE +1.14%)
   - −2.0% : fill 30min 22% · séance 46% (71/159) · gap 5% · délai 30.1min · rebond 61% (42/71) (MFE +1.31%)
   - −3.0% : fill 30min 10% · séance 31% (47/159) · gap 3% · délai 119.0min · rebond 60% (29/47) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 22% (28/159) · gap 2% · délai 152.6min · rebond 61% (16/28) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 11% (16/159) · gap 1% · délai 206.9min · rebond 48% (8/16) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.73% (p90 −1.65%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −1.76%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.77%) → stop au-delà de −1.59% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=462 jambes) : jambe baissière méd −1.07% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 94% (51/53) · rebond 62% (28/51)
      · −2.0% : fill 77% (40/53) · rebond 63% (25/40)
      · −3.0% : fill 50% (28/53) · rebond 59% (18/28)
      · −4.0% : fill 36% (16/53) · rebond 71% (11/16)
      · −5.0% : fill 17% (9/53) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 71% (36/50) · rebond 69% (24/36)
      · −2.0% : fill 30% (17/50) · rebond 72% (10/17)
      · −3.0% : fill 20% (10/50) · rebond 55% (5/10)
      · −4.0% : fill 18% (8/50) · rebond 36% (2/8)
      · −5.0% : fill 12% (6/50) · rebond 22% (1/6)
   - **gap-up** (56 séances) :
      · −1.0% : fill 46% (23/56) · rebond 49% (12/23)
      · −2.0% : fill 28% (14/56) · rebond 46% (7/14)
      · −3.0% : fill 22% (9/56) · rebond 66% (6/9)
      · −4.0% : fill 12% (4/56) · rebond 61% (3/4)
      · −5.0% : fill 4% (1/56) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 68% si les 15 1res min sont vertes (84 cas) · 36% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 76% si début vert vs 27% si rouge (base 51% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **76%** · continue >prix actuel 49% ; creux résiduel méd -1.25% (q20 -2.17%) → **SL/trailing à −2.17%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.25% / q75 +1.88% → **scale +1.25% / runner +1.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **27%** (continue à baisser 53%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.98%** (au-delà de la MAE q10 -4.98%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +3.08%] · haut q95 +3.76% · bas q05 -3.16%
   - 60min (n=160) : retour [-3.38% .. +3.06%] · haut q95 +3.95% · bas q05 -3.96%
   - 2h (n=160) : retour [-3.57% .. +2.79%] · haut q95 +4.08% · bas q05 -4.54%
   - 4h (n=160) : retour [-3.71% .. +2.96%] · haut q95 +4.45% · bas q05 -5.06%
   - 6h (n=160) : retour [-4.66% .. +3.18%] · haut q95 +4.53% · bas q05 -5.72%
   - session (n=160) : retour [-6.18% .. +4.16%] · haut q95 +4.74% · bas q05 -6.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.8  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 9.303  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 20.6%
- **ATR** : 42.12 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.14  _(accumulation)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 39.2  _(transition)_
- **MA** : MA20 1022.87 · MA50 1117.45 · MA200 1477.75  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 -7.1% · MA200 -29.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90400 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
