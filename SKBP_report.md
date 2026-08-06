# 326030

**Generated** : 2026-08-06T21:57:24.088914+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩83200.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩83200.00 (+0.5% vs entrée) · entrée ₩82808.33 · stop ₩81566.21 · T1 ₩84196.01 · R/R 1.12  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.151 _(réel 5 s)_ (GBM -0.011) · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.080 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩82530.80–₩83085.87 (mid ₩82808.33)
- Spot actuel : ₩83200.00 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : ₩81566.21 (stop swing_plan-based (-5.97%))
- Targets : T1 ₩84196.01 · R/R 1.12 | T2 ₩85583.69 · R/R 2.23 | T3 ₩86971.37 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩81566.21


## Edge, scénarios & sizing

- EV/risk : -0.011 | EV/share : ₩-14.214 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 23 % | T3 9 %
- Kelly (position) : f* 0.025 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 51.5 | bear 37.9 | side 10.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.467% → cible +1.676% / stop −1.5%, p_fill 76%, n_eff≈33.9) : P(cible|rempli) **40%** · **EV/risk -0.151** (×p_fill ; si rempli -0.30% du capital)
  - **swing** (entrée dip −1.033% → cible +3.747% / stop −4.988%, p_fill 74%, n_eff≈32.2) : P(cible|rempli) **44%** · **EV/risk -0.143** (×p_fill ; si rempli -0.97% du capital)
  - **deep** (entrée dip −1.606% → cible +5.299% / stop −7.525%, p_fill 81%, n_eff≈34.8) : P(cible|rempli) **50%** · **EV/risk -0.095** (×p_fill ; si rempli -0.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→46% · +3.0%→32% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.33% (p90 7.69%) · excursion haute méd. +1.72% / basse méd. −2.34%
- Profil de vol intra : ouverture 2.907% vs midi 0.872% vs clôture 0.869% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (148 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 12% · trend ↑1%/↓1% ; spike-down 56% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.093)_ ; drift intra méd. -0.014% ; recovery-V 31%
- **σ réalisé intraday** 3.551% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 53% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 82753.75 (VA 82488.75–84078.75 ; dernier close 82100.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 70% · **stop −4.04%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.39 (high win-rate)
- Gaps overnight (n=147) : méd. 0.1% · baisse 42% (gap-down >1% 18% · >2% 8%)
- Excursion ouverture 5min (n=148) : bas méd −0.77% (p90 −2.28%) · haut méd +0.71% · range méd 2.05%
- Excursion ouverture 15min (n=148) : bas méd −0.95% (p90 −2.94%) · haut méd +0.82% · range méd 2.3%
- Excursion ouverture 30min (n=148) : bas méd −1.09% (p90 −2.97%) · haut méd +1.12% · range méd 2.66%
- Excursion ouverture 60min (n=148) : bas méd −1.17% (p90 −3.13%) · haut méd +1.44% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 82100.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 78% (108/147) · gap 28% · délai 0.2min · rebond 55% (48/108) (MFE +1.29%)
   - −1.0% : fill 30min 55% · séance 67% (96/147) · gap 18% · délai 1.1min · rebond 57% (47/96) (MFE +1.22%)
   - −1.5% : fill 30min 41% · séance 54% (73/147) · gap 10% · délai 1.4min · rebond 64% (39/73) (MFE +1.42%)
   - −2.0% : fill 30min 30% · séance 46% (61/147) · gap 8% · délai 8.3min · rebond 70% (36/61) (MFE +1.56%)
   - −3.0% : fill 30min 12% · séance 34% (40/147) · gap 3% · délai 79.9min · rebond 58% (18/40) (MFE +1.39%)
   - −4.0% : fill 30min 6% · séance 21% (27/147) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 5% · séance 15% (20/147) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.78%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.42%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.46% (p90 −1.41%) → stop au-delà de −1.19% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=516 jambes) : jambe baissière méd −1.09% (p90 −2.48%) · ~10.2 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 95% (44/45) · rebond 66% (24/44)
      · −2.0% : fill 70% (31/45) · rebond 70% (17/31)
      · −3.0% : fill 46% (20/45) · rebond 61% (9/20)
      · −4.0% : fill 35% (16/45) · rebond 70% (9/16)
      · −5.0% : fill 23% (12/45) · rebond 85% (8/12)
   - **flat** (39 séances) :
      · −1.0% : fill 67% (27/39) · rebond 47% (11/27)
      · −2.0% : fill 51% (19/39) · rebond 77% (13/19)
      · −3.0% : fill 40% (12/39) · rebond 61% (6/12)
      · −4.0% : fill 31% (9/39) · rebond 50% (4/9)
      · −5.0% : fill 24% (7/39) · rebond 84% (5/7)
   - **gap-up** (63 séances) :
      · −1.0% : fill 44% (25/63) · rebond 53% (12/25)
      · −2.0% : fill 24% (11/63) · rebond 56% (6/11)
      · −3.0% : fill 18% (8/63) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/63) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/63) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=148) : 43% en base · 73% si les 15 1res min sont vertes (54 cas) · 22% si rouges (94 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=148) : COUDE à **54min** → P(séance verte=clôture>ouverture) 78% si début vert vs 11% si rouge (base 43% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **78%** · continue >prix actuel 51% ; creux résiduel méd -1.65% (q20 -3.09%) → **SL/trailing à −3.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.52% / q75 +2.6% → **scale +1.52% / runner +2.6%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.29%** (au-delà de la MAE q10 -4.29%), cible rebond +1.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=148) : retour [-2.71% .. +3.6%] · haut q95 +3.97% · bas q05 -3.75%
   - 60min (n=148) : retour [-3.36% .. +4.25%] · haut q95 +5.6% · bas q05 -4.06%
   - 2h (n=148) : retour [-3.31% .. +4.77%] · haut q95 +5.67% · bas q05 -4.39%
   - 4h (n=148) : retour [-4.37% .. +5.94%] · haut q95 +6.72% · bas q05 -5.93%
   - 6h (n=148) : retour [-4.93% .. +4.74%] · haut q95 +7.57% · bas q05 -6.28%
   - session (n=148) : retour [-4.96% .. +5.1%] · haut q95 +7.57% · bas q05 -6.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.8  _(momentum haussier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist 846.082  _(pas de croisement recent)_
- **BB** : %B 0.95 · largeur 11.4%
- **ATR** : 4107.14 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.083  _(distribution)_
- **Vol ratio** : 1.15  _(volume normal)_
- **Choppiness** : 55.5  _(transition)_
- **MA** : MA20 79130.0 · MA50 84254.0 · MA200 105694.5  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 -1.3% · MA200 -21.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83726 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
