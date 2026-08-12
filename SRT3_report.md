# SRT3

**Generated** : 2026-08-12T21:37:29.899721+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €236.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €236.00 (+3.1% vs entrée) · entrée €228.94 · stop €219.60 · T1 €236.32 · R/R 0.79  
> ↳ P(T1 av. stop) 66 % _(réel 5 s)_ · EV/risk 0.059 _(réel 5 s)_ (GBM 0.029) · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €227.46–€230.42 (mid €228.94)
- Spot actuel : €236.00 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : €219.60 (stop swing_plan-based (-6.95%))
- Targets : T1 €236.32 · R/R 0.79 | T2 €243.69 · R/R 1.58 | T3 €251.07 · R/R 2.37
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €219.60


## Edge, scénarios & sizing

- EV/risk : 0.029 | EV/share : €0.275 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 26 % | T3 8 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈215) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 25.8 | bear 49.7 | side 24.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 236.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.36% → cible +1.441% / stop −1.5%, p_fill 48%, n_eff≈21.1) : P(cible|rempli) **40%** · **EV/risk -0.054** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −2.991% → cible +3.222% / stop −4.081%, p_fill 39%, n_eff≈15.4) : P(cible|rempli) **66%** · **EV/risk +0.059** (×p_fill ; si rempli +0.62% du capital)
  - **deep** (entrée dip −4.622% → cible +4.557% / stop −6.226%, p_fill 46%, n_eff≈15.7) : P(cible|rempli) **67%** · **EV/risk +0.061** (×p_fill ; si rempli +0.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→48% · +3.0%→25% · +5.0%→6% · +8.0%→0%
- Range intraday médian 3.57% (p90 6.83%) · excursion haute méd. +1.94% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.156% vs midi 0.913% vs clôture 1.011% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.103 ; neutre — autocorr -0.013)_ ; drift intra méd. 0.142% ; recovery-V 34%
- **σ réalisé intraday** 2.717% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 75% / bas 69% / whipsaw 46%
- POC intraday (dernière séance, temps-au-prix) : 236.1712 (VA 234.4387–237.2738 ; dernier close 238.3)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 74% · **stop −2.38%** sous le fill (sous le bruit) · cible +1.79% · R/R 0.75 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 51% (gap-down >1% 14% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.35% (p90 −1.92%) · haut méd +0.58% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.99%) · haut méd +0.67% · range méd 1.52%
- Excursion ouverture 30min (n=160) : bas méd −0.56% (p90 −2.35%) · haut méd +0.87% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −2.74%) · haut méd +0.95% · range méd 1.86%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 238.3 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 77% (124/159) · gap 26% · délai 0.2min · rebond 56% (65/124) (MFE +1.2%)
   - −1.0% : fill 30min 42% · séance 65% (105/159) · gap 14% · délai 2.6min · rebond 61% (61/105) (MFE +1.42%)
   - −1.5% : fill 30min 35% · séance 57% (95/159) · gap 7% · délai 4.8min · rebond 74% (62/95) (MFE +1.79%)
   - −2.0% : fill 30min 21% · séance 41% (74/159) · gap 4% · délai 32.2min · rebond 66% (46/74) (MFE +1.96%)
   - −3.0% : fill 30min 6% · séance 18% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 10% (21/159) · gap 0% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 0% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.21%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.16% (p90 −2.4%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.73%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=430 jambes) : jambe baissière méd −1.04% (p90 −2.55%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 78% (58/71) · rebond 68% (37/58)
      · −2.0% : fill 50% (42/71) · rebond 64% (27/42)
      · −3.0% : fill 29% (28/71) · rebond 48% (15/28)
      · −4.0% : fill 14% (15/71) · rebond 71% (11/15)
      · −5.0% : fill 7% (7/71) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 65% (21/34) · rebond 61% (11/21)
      · −2.0% : fill 50% (16/34) · rebond 62% (8/16)
      · −3.0% : fill 17% (6/34) · rebond 66% (4/6)
      · −4.0% : fill 13% (4/34) · rebond 70% (3/4)
      · −5.0% : fill 13% (4/34) · rebond 24% (2/4)
   - **gap-up** (54 séances) :
      · −1.0% : fill 52% (26/54) · rebond 50% (13/26)
      · −2.0% : fill 26% (16/54) · rebond 77% (11/16)
      · −3.0% : fill 7% (6/54) · rebond 78% (4/6)
      · −4.0% : fill 5% (2/54) · rebond 100% (2/2)
      · −5.0% : fill 4% (1/54) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 58% si les 15 1res min sont vertes (90 cas) · 43% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 71% si début vert vs 27% si rouge (base 52% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=81) : tient le vert **71%** · continue >prix actuel 48% ; creux résiduel méd -1.13% (q20 -1.86%) → **SL/trailing à −1.86%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.11% / q75 +2.28% → **scale +1.11% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **27%** (continue à baisser 52%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.34%** (au-delà de la MAE q10 -3.34%), cible rebond +1.44% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.99% .. +2.19%] · haut q95 +2.64% · bas q05 -3.48%
   - 60min (n=160) : retour [-3.17% .. +2.36%] · haut q95 +2.88% · bas q05 -3.83%
   - 2h (n=160) : retour [-2.23% .. +2.55%] · haut q95 +2.98% · bas q05 -3.85%
   - 4h (n=160) : retour [-2.56% .. +2.29%] · haut q95 +3.32% · bas q05 -3.87%
   - 6h (n=160) : retour [-2.68% .. +3.04%] · haut q95 +3.78% · bas q05 -5.54%
   - session (n=160) : retour [-3.7% .. +4.17%] · haut q95 +5.71% · bas q05 -5.54%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.33%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 67.6  _(momentum haussier)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist 1.418  _(pas de croisement recent)_
- **BB** : %B 0.66 · largeur 17.0%
- **ATR** : 9.34 (67.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.116  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 229.86 · MA50 230.34 · MA200 231.96  _(prix > MA20)_
- **Dist MA** : MA20 +2.7% · MA50 +2.5% · MA200 +1.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93020 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
