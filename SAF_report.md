# SAF

**Generated** : 2026-08-18T21:41:36.559901+00:00  
**Santé technique** : 8/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €353.10  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €353.10 (+1.2% vs entrée) · entrée €348.90 · stop €341.34 · T1 €360.80 · R/R 1.57  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk 0.226 _(réel 5 s)_ (GBM 0.083) · ¼-Kelly 0.004 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €347.55–€350.26 (mid €348.90)
- Spot actuel : €353.10 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €341.34 (stop swing_plan-based (-3.33%))
- Targets : T1 €360.80 · R/R 1.57 | T2 €364.97 · R/R 2.13 | T3 €369.13 · R/R 2.68
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €341.34


## Edge, scénarios & sizing

- EV/risk : 0.083 | EV/share : €0.624 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 24 % | T3 18 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.1 | bear 10.4 | side 84.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 353.0 (= 1 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.541% → cible +2.475% / stop −2.0%, p_fill 74%, n_eff≈30.0) : P(cible|rempli) **6%** · **EV/risk -0.043** (×p_fill ; si rempli -0.12% du capital)
  - **swing** (entrée dip −1.188% → cible +3.41% / stop −2.168%, p_fill 63%, n_eff≈25.1) : P(cible|rempli) **39%** · **EV/risk +0.226** (×p_fill ; si rempli +0.77% du capital)
  - **deep** (entrée dip −1.837% → cible +2.733% / stop −3.274%, p_fill 52%, n_eff≈23.0) : P(cible|rempli) **68%** · **EV/risk +0.108** (×p_fill ; si rempli +0.68% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→56% · +2.0%→31% · +3.0%→12% · +5.0%→1% · +8.0%→1%
- Range intraday médian 2.54% (p90 4.15%) · excursion haute méd. +1.27% / basse méd. −0.88%
- Profil de vol intra : ouverture 1.576% vs midi 0.573% vs clôture 0.707% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 39% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.098 ; mean-reverting — autocorr -0.047)_ ; drift intra méd. 0.041% ; recovery-V 26%
- **σ réalisé intraday** 1.71% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 75% / bas 53% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 361.15 (VA 359.71–361.75 ; dernier close 361.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 29% · rebond 52% · **stop −2.07%** sous le fill (sous le bruit) · cible +1.14% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.14% · baisse 44% (gap-down >1% 8% · >2% 1%)
- Excursion ouverture 5min (n=160) : bas méd −0.43% (p90 −1.72%) · haut méd +0.19% · range méd 0.92%
- Excursion ouverture 15min (n=160) : bas méd −0.55% (p90 −1.92%) · haut méd +0.31% · range méd 1.15%
- Excursion ouverture 30min (n=160) : bas méd −0.6% (p90 −1.92%) · haut méd +0.52% · range méd 1.31%
- Excursion ouverture 60min (n=160) : bas méd −0.67% (p90 −1.96%) · haut méd +0.56% · range méd 1.54%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 361.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 67% (112/159) · gap 19% · délai 0.2min · rebond 42% (44/112) (MFE +0.81%)
   - −1.0% : fill 30min 36% · séance 48% (84/159) · gap 8% · délai 0.6min · rebond 44% (32/84) (MFE +0.67%)
   - −1.5% : fill 30min 24% · séance 39% (70/159) · gap 3% · délai 12.6min · rebond 43% (26/70) (MFE +0.9%)
   - −2.0% : fill 30min 11% · séance 29% (52/159) · gap 1% · délai 52.5min · rebond 52% (24/52) (MFE +1.14%)
   - −3.0% : fill 30min 3% · séance 15% (29/159) · gap 0% · délai 87.1min · rebond 54% (17/29) (MFE +1.2%)
   - −4.0% : fill 30min 2% · séance 6% (13/159) · gap 0% · délai 126.9min · rebond 62% (7/13) (MFE +1.25%)
   - −5.0% : fill 30min 0% · séance 1% (3/159) · gap 0% · délai 360.2min · rebond 31% (1/3) (MFE +1.0%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.17% (p90 −0.81%) → stop au-delà de −0.69% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −0.78%) → stop au-delà de −0.62% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.11% (p90 −0.96%) → stop au-delà de −0.79% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=210 jambes) : jambe baissière méd −1.04% (p90 −2.34%) · ~5.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 83% (45/55) · rebond 41% (17/45)
      · −2.0% : fill 60% (32/55) · rebond 48% (15/32)
      · −3.0% : fill 29% (17/55) · rebond 50% (9/17)
      · −4.0% : fill 15% (9/55) · rebond 69% (5/9)
      · −5.0% : fill 2% (2/55) · rebond 0% (0/2)
   - **flat** (41 séances) :
      · −1.0% : fill 40% (19/41) · rebond 56% (10/19)
      · −2.0% : fill 19% (9/41) · rebond 75% (5/9)
      · −3.0% : fill 10% (5/41) · rebond 85% (4/5)
      · −4.0% : fill 1% (1/41) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/41) · rebond 0% (0/0)
   - **gap-up** (63 séances) :
      · −1.0% : fill 28% (20/63) · rebond 36% (5/20)
      · −2.0% : fill 13% (11/63) · rebond 43% (4/11)
      · −3.0% : fill 8% (7/63) · rebond 36% (4/7)
      · −4.0% : fill 4% (3/63) · rebond 30% (1/3)
      · −5.0% : fill 1% (1/63) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 66% si les 15 1res min sont vertes (75 cas) · 33% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **44min** → P(séance verte=clôture>ouverture) 75% si début vert vs 25% si rouge (base 50% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **75%** · continue >prix actuel 54% ; creux résiduel méd -0.73% (q20 -1.44%) → **SL/trailing à −1.44%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.9% / q75 +1.58% → **scale +0.9% / runner +1.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **25%** (continue à baisser 48%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.4%** (au-delà de la MAE q10 -2.4%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.59% .. +1.58%] · haut q95 +1.98% · bas q05 -2.21%
   - 60min (n=160) : retour [-1.63% .. +2.14%] · haut q95 +2.33% · bas q05 -2.5%
   - 2h (n=160) : retour [-2.26% .. +2.2%] · haut q95 +2.6% · bas q05 -2.94%
   - 4h (n=160) : retour [-2.01% .. +2.19%] · haut q95 +2.79% · bas q05 -3.06%
   - 6h (n=160) : retour [-2.16% .. +2.48%] · haut q95 +3.14% · bas q05 -3.36%
   - session (n=160) : retour [-2.94% .. +2.61%] · haut q95 +3.52% · bas q05 -4.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SAF = **plat / peu volatil** (vol intra méd 1.69%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 62.2  _(momentum haussier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist -0.092  _(bearish_recent)_
- **BB** : %B 0.58 · largeur 15.3%
- **ATR** : 7.56 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.013  _(neutre)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 46.9  _(transition)_
- **MA** : MA20 348.65 · MA50 338.39 · MA200 308.68  _(prix > MA20)_
- **Dist MA** : MA20 +1.3% · MA50 +4.3% · MA200 +14.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92161 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
