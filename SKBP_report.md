# 326030

**Generated** : 2026-08-04T21:57:14.772844+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · ₩79700.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩79700.00 (+1.8% vs entrée) · entrée ₩78275.00 · stop ₩76595.83 · T1 ₩81633.33 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.139 _(réel 5 s)_ (GBM -0.182) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.15% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩78011.01–₩78538.99 (mid ₩78275.00)
- Spot actuel : ₩79700.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩76595.83 (stop swing_plan-based (-8.91%))
- Targets : T1 ₩81633.33 · R/R 2.0 | T2 ₩81928.13 · R/R 2.18 | T3 ₩82222.92 · R/R 2.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩76595.83


## Edge, scénarios & sizing

- EV/risk : -0.182 | EV/share : ₩-306.273 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 10 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 32.5 | bear 59.6 | side 7.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.783% → cible +4.29% / stop −2.145%, p_fill 58%, n_eff≈23.9) : P(cible|rempli) **3%** · **EV/risk -0.139** (×p_fill ; si rempli -0.52% du capital)
  - **swing** (entrée dip −3.936% → cible +3.759% / stop −5.178%, p_fill 41%, n_eff≈18.3) : P(cible|rempli) **54%** · **EV/risk -0.002** (×p_fill ; si rempli -0.02% du capital)
  - **deep** (entrée dip −6.079% → cible +5.316% / stop −7.944%, p_fill 42%, n_eff≈18.4) : P(cible|rempli) **73%** · **EV/risk +0.085** (×p_fill ; si rempli +1.60% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→45% · +3.0%→31% · +5.0%→10% · +8.0%→5%
- Range intraday médian 4.3% (p90 7.69%) · excursion haute méd. +1.65% / basse méd. −2.34%
- Profil de vol intra : ouverture 2.88% vs midi 0.856% vs clôture 0.863% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (146 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 13% · trend ↑1%/↓1% ; spike-down 58% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.098)_ ; drift intra méd. -0.14% ; recovery-V 26%
- **σ réalisé intraday** 3.485% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 58% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 77993.75 (VA 77643.75–79043.75 ; dernier close 77800.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 15% · rebond 83% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.82% · R/R 0.65 (high win-rate)
- Gaps overnight (n=145) : méd. 0.05% · baisse 43% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=146) : bas méd −0.77% (p90 −2.3%) · haut méd +0.72% · range méd 2.06%
- Excursion ouverture 15min (n=146) : bas méd −0.95% (p90 −2.94%) · haut méd +0.82% · range méd 2.31%
- Excursion ouverture 30min (n=146) : bas méd −1.1% (p90 −2.98%) · haut méd +1.12% · range méd 2.66%
- Excursion ouverture 60min (n=146) : bas méd −1.22% (p90 −3.16%) · haut méd +1.34% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 77800.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 81% (108/145) · gap 29% · délai 0.2min · rebond 55% (48/108) (MFE +1.29%)
   - −1.0% : fill 30min 57% · séance 70% (96/145) · gap 18% · délai 1.1min · rebond 57% (47/96) (MFE +1.22%)
   - −1.5% : fill 30min 43% · séance 56% (73/145) · gap 10% · délai 1.4min · rebond 64% (39/73) (MFE +1.42%)
   - −2.0% : fill 30min 31% · séance 48% (61/145) · gap 8% · délai 8.3min · rebond 70% (36/61) (MFE +1.56%)
   - −3.0% : fill 30min 13% · séance 35% (40/145) · gap 3% · délai 79.9min · rebond 58% (18/40) (MFE +1.39%)
   - −4.0% : fill 30min 6% · séance 22% (27/145) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 5% · séance 15% (20/145) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.84%) → stop au-delà de −1.4% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −1.41%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=505 jambes) : jambe baissière méd −1.11% (p90 −2.48%) · ~10.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 66% (24/44)
      · −2.0% : fill 70% (31/45) · rebond 70% (17/31)
      · −3.0% : fill 46% (20/45) · rebond 61% (9/20)
      · −4.0% : fill 35% (16/45) · rebond 70% (9/16)
      · −5.0% : fill 23% (12/45) · rebond 85% (8/12)
   - **flat** (38 séances) :
      · −1.0% : fill 71% (27/38) · rebond 47% (11/27)
      · −2.0% : fill 54% (19/38) · rebond 77% (13/19)
      · −3.0% : fill 43% (12/38) · rebond 61% (6/12)
      · −4.0% : fill 33% (9/38) · rebond 50% (4/9)
      · −5.0% : fill 25% (7/38) · rebond 84% (5/7)
   - **gap-up** (62 séances) :
      · −1.0% : fill 46% (25/62) · rebond 53% (12/25)
      · −2.0% : fill 25% (11/62) · rebond 56% (6/11)
      · −3.0% : fill 19% (8/62) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/62) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/62) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=146) : 41% en base · 72% si les 15 1res min sont vertes (53 cas) · 19% si rouges (93 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=146) : COUDE à **45min** → P(séance verte=clôture>ouverture) 76% si début vert vs 10% si rouge (base 41% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **76%** · continue >prix actuel 47% ; creux résiduel méd -1.54% (q20 -3.07%) → **SL/trailing à −3.07%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.22% → **scale +1.29% / runner +2.22%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **10%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.65%** (au-delà de la MAE q10 -3.65%), cible rebond +1.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=146) : retour [-2.73% .. +3.77%] · haut q95 +4.06% · bas q05 -3.82%
   - 60min (n=146) : retour [-3.58% .. +4.0%] · haut q95 +4.65% · bas q05 -4.13%
   - 2h (n=146) : retour [-3.35% .. +4.44%] · haut q95 +5.18% · bas q05 -4.44%
   - 4h (n=146) : retour [-4.4% .. +6.1%] · haut q95 +6.86% · bas q05 -5.96%
   - 6h (n=146) : retour [-5.11% .. +4.93%] · haut q95 +7.73% · bas q05 -6.35%
   - session (n=146) : retour [-4.99% .. +5.12%] · haut q95 +7.73% · bas q05 -6.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.39%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 59.9  _(momentum haussier)_
- **ADX** : 19.8  _(pas de tendance nette)_
- **MACD** : hist 438.745  _(pas de croisement recent)_
- **BB** : %B 0.55 · largeur 12.4%
- **ATR** : 3964.29 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.072  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 63.8  _(marche en range (choppy))_
- **MA** : MA20 79215.0 · MA50 84838.0 · MA200 105887.5  _(prix > MA20)_
- **Dist MA** : MA20 +0.6% · MA50 -6.1% · MA200 -24.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84132 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
