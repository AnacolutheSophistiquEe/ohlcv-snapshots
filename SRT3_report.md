# SRT3

**Generated** : 2026-07-03T21:37:24.084553+00:00  
**Santé technique** : 5/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €226.60  

> 🟡 **WAIT-FOR-DIP** — spot +1.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €226.60 (+1.9% vs entrée) · entrée €222.41 · stop €218.93 · T1 €229.37 · R/R 2.0  
> ↳ P(T1 av. stop) 54 % _(réel 5 s)_ · EV/risk 0.367 _(réel 5 s)_ (GBM 0.002) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.170 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €221.01–€223.80 (mid €222.41)
- Spot actuel : €226.60 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €218.93 (stop swing_plan-based (-3.39%))
- Targets : T1 €229.37 · R/R 2.0 | T2 €236.33 · R/R 4.0 | T3 €243.29 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €218.93


## Edge, scénarios & sizing

- EV/risk : 0.002 | EV/share : €0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.012 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 50.0 | bear 16.9 | side 33.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 227.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.845% → cible +1.4% / stop −3.0%, p_fill 68%, n_eff≈27.3) : P(cible|rempli) **44%** · **EV/risk -0.022** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −1.854% → cible +3.13% / stop −1.565%, p_fill 64%, n_eff≈26.4) : P(cible|rempli) **54%** · **EV/risk +0.367** (×p_fill ; si rempli +0.89% du capital)
  - **deep** (entrée dip −2.86% → cible +4.426% / stop −2.213%, p_fill 67%, n_eff≈23.3) : P(cible|rempli) **39%** · **EV/risk +0.078** (×p_fill ; si rempli +0.26% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→71% · +2.0%→45% · +3.0%→24% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.61% (p90 6.59%) · excursion haute méd. +1.84% / basse méd. −1.92%
- Profil de vol intra : ouverture 2.035% vs midi 0.881% vs clôture 1.01% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 7% · trend ↑1%/↓0% ; spike-down 54% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.02)_ ; drift intra méd. 0.152% ; recovery-V 29%
- **σ réalisé intraday** 2.394% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 229.8594 (VA 228.4531–231.4219 ; dernier close 231.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 68% · **stop −2.59%** sous le fill (sous le bruit) · cible +1.57% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 52% (gap-down >1% 18% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.31% (p90 −1.78%) · haut méd +0.57% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.88%) · haut méd +0.68% · range méd 1.47%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.02%) · haut méd +0.83% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.36%) · haut méd +0.94% · range méd 1.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 231.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 76% (122/159) · gap 28% · délai 0.2min · rebond 53% (57/122) (MFE +1.11%)
   - −1.0% : fill 30min 44% · séance 64% (103/159) · gap 18% · délai 0.6min · rebond 60% (58/103) (MFE +1.26%)
   - −1.5% : fill 30min 33% · séance 57% (90/159) · gap 11% · délai 14.0min · rebond 68% (55/90) (MFE +1.57%)
   - −2.0% : fill 30min 22% · séance 42% (68/159) · gap 6% · délai 24.7min · rebond 61% (43/68) (MFE +1.43%)
   - −3.0% : fill 30min 6% · séance 23% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 12% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 7% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.22% (p90 −1.84%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.17% (p90 −1.89%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.18% (p90 −2.2%) → stop au-delà de −1.45% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.04% (p90 −2.37%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 85% (62/75) · rebond 68% (39/62)
      · −2.0% : fill 60% (42/75) · rebond 65% (28/42)
      · −3.0% : fill 39% (29/75) · rebond 56% (17/29)
      · −4.0% : fill 21% (16/75) · rebond 71% (12/16)
      · −5.0% : fill 11% (7/75) · rebond 92% (6/7)
   - **flat** (36 séances) :
      · −1.0% : fill 59% (20/36) · rebond 40% (9/20)
      · −2.0% : fill 44% (14/36) · rebond 45% (7/14)
      · −3.0% : fill 19% (6/36) · rebond 49% (4/6)
      · −4.0% : fill 12% (3/36) · rebond 44% (2/3)
      · −5.0% : fill 12% (3/36) · rebond 44% (2/3)
   - **gap-up** (48 séances) :
      · −1.0% : fill 42% (21/48) · rebond 58% (10/21)
      · −2.0% : fill 18% (12/48) · rebond 72% (8/12)
      · −3.0% : fill 6% (5/48) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/48) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/48) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 62% si les 15 1res min sont vertes (90 cas) · 44% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 80% si début vert vs 30% si rouge (base 55% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **80%** · continue >prix actuel 57% ; creux résiduel méd -0.87% (q20 -2.19%) → **SL/trailing à −2.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +2.2% → **scale +1.18% / runner +2.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **30%** (continue à baisser 49%) → **RÉDUIRE ~70%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.07%** (au-delà de la MAE q10 -3.07%), cible rebond +1.29% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.17% .. +2.11%] · haut q95 +2.64% · bas q05 -2.76%
   - 60min (n=160) : retour [-2.51% .. +2.32%] · haut q95 +2.78% · bas q05 -3.17%
   - 2h (n=160) : retour [-2.26% .. +2.6%] · haut q95 +3.1% · bas q05 -3.19%
   - 4h (n=160) : retour [-2.69% .. +2.6%] · haut q95 +3.28% · bas q05 -3.54%
   - 6h (n=160) : retour [-2.72% .. +3.49%] · haut q95 +3.96% · bas q05 -3.87%
   - session (n=160) : retour [-3.6% .. +4.59%] · haut q95 +5.63% · bas q05 -4.5%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.21%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 13.2  _(pas de tendance nette)_
- **MACD** : hist 0.099  _(bullish_recent)_
- **BB** : %B 0.47 · largeur 16.9%
- **ATR** : 9.73 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.172  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 51.6  _(transition)_
- **MA** : MA20 227.89 · MA50 225.87 · MA200 229.33  _(prix < MA20)_
- **Dist MA** : MA20 -0.6% · MA50 +0.3% · MA200 -1.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94389 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
