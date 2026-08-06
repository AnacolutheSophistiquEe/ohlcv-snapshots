# 326030

**Generated** : 2026-08-06T00:20:19.326871+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩82000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩82000.00 (+0.3% vs entrée) · entrée ₩81736.28 · stop ₩80510.24 · T1 ₩83138.87 · R/R 1.14  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk -0.162 _(réel 5 s)_ (GBM -0.027) · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩81472.57–₩82000.00 (mid ₩81736.28)
- Spot actuel : ₩82000.00 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : ₩80510.24 (stop swing_plan-based (-5.47%))
- Targets : T1 ₩83138.87 · R/R 1.14 | T2 ₩84541.46 · R/R 2.29 | T3 ₩85944.05 · R/R 3.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩80510.24


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : ₩-32.579 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 21 % | T3 8 %
- Kelly (position) : f* 0.018 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.4 | bear 6.2 | side 77.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.325% → cible +1.716% / stop −1.5%, p_fill 82%, n_eff≈36.6) : P(cible|rempli) **39%** · **EV/risk -0.162** (×p_fill ; si rempli -0.30% du capital)
  - **swing** (entrée dip −0.531% → cible +3.837% / stop −4.966%, p_fill 80%, n_eff≈35.3) : P(cible|rempli) **34%** · **EV/risk -0.243** (×p_fill ; si rempli -1.50% du capital)
  - **deep** (entrée dip −0.731% → cible +5.426% / stop −7.463%, p_fill 87%, n_eff≈36.7) : P(cible|rempli) **38%** · **EV/risk -0.301** (×p_fill ; si rempli -2.59% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.8  _(momentum haussier)_
- **ADX** : 18.9  _(pas de tendance nette)_
- **MACD** : hist 653.458  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 11.0%
- **ATR** : 4050.0 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.125  _(distribution)_
- **Vol ratio** : 1.54  _(volume au-dessus de la moyenne)_
- **Choppiness** : 54.9  _(transition)_
- **MA** : MA20 79075.0 · MA50 84524.0 · MA200 105786.0  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 -3.0% · MA200 -22.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84268 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
