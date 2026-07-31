# SRT3

**Generated** : 2026-07-31T21:37:27.586290+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €218.00  

> 🟡 **WAIT-FOR-DIP** — spot +5.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €218.00 (+5.1% vs entrée) · entrée €207.34 · stop €203.83 · T1 €211.11 · R/R 1.07  
> ↳ P(T1 av. stop) 45 % · EV/risk 0.003 · ¼-Kelly 0.006 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.69% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.090 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €206.58–€208.09 (mid €207.34)
- Spot actuel : €218.00 (+5.1% au-dessus de la zone — repli à attendre)
- Stop : €203.83 (stop swing_plan-based (-12.58%))
- Targets : T1 €211.11 · R/R 1.07 | T2 €214.88 · R/R 2.15 | T3 €218.65 · R/R 3.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €203.83


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : €0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 16 % | T3 9 %
- Kelly (position) : f* 0.024 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.2 | bear 74.7 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→75% · +2.0%→46% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.65% (p90 7.16%) · excursion haute méd. +1.89% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.154% vs midi 0.912% vs clôture 1.034% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 11% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; neutre — autocorr 0.007)_ ; drift intra méd. -0.1% ; recovery-V 32%
- **σ réalisé intraday** 2.939% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 65% / whipsaw 36%
- POC intraday (dernière séance, temps-au-prix) : 223.6413 (VA 222.3663–224.7887 ; dernier close 225.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 61% · rebond 75% · **stop −2.5%** sous le fill (sous le bruit) · cible +1.86% · R/R 0.74 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 51% (gap-down >1% 16% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −2.47%) · haut méd +0.57% · range méd 1.3%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −2.48%) · haut méd +0.66% · range méd 1.61%
- Excursion ouverture 30min (n=160) : bas méd −0.63% (p90 −2.78%) · haut méd +0.77% · range méd 1.76%
- Excursion ouverture 60min (n=160) : bas méd −0.74% (p90 −2.81%) · haut méd +0.78% · range méd 1.92%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 225.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 81% (126/159) · gap 29% · délai 0.2min · rebond 58% (66/126) (MFE +1.2%)
   - −1.0% : fill 30min 48% · séance 67% (105/159) · gap 16% · délai 0.3min · rebond 64% (64/105) (MFE +1.48%)
   - −1.5% : fill 30min 39% · séance 61% (92/159) · gap 8% · délai 3.1min · rebond 75% (60/92) (MFE +1.86%)
   - −2.0% : fill 30min 24% · séance 44% (72/159) · gap 4% · délai 17.5min · rebond 63% (44/72) (MFE +1.96%)
   - −3.0% : fill 30min 8% · séance 21% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 12% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 9% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −2.37%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −2.44%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.8%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=426 jambes) : jambe baissière méd −1.05% (p90 −2.72%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 86% (62/74) · rebond 72% (42/62)
      · −2.0% : fill 57% (42/74) · rebond 64% (27/42)
      · −3.0% : fill 33% (28/74) · rebond 48% (15/28)
      · −4.0% : fill 16% (15/74) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/74) · rebond 92% (6/7)
   - **flat** (35 séances) :
      · −1.0% : fill 58% (19/35) · rebond 50% (9/19)
      · −2.0% : fill 49% (15/35) · rebond 55% (7/15)
      · −3.0% : fill 20% (6/35) · rebond 66% (4/6)
      · −4.0% : fill 15% (4/35) · rebond 70% (3/4)
      · −5.0% : fill 15% (4/35) · rebond 24% (2/4)
   - **gap-up** (50 séances) :
      · −1.0% : fill 52% (24/50) · rebond 60% (13/24)
      · −2.0% : fill 27% (15/50) · rebond 72% (10/15)
      · −3.0% : fill 9% (6/50) · rebond 78% (4/6)
      · −4.0% : fill 6% (2/50) · rebond 100% (2/2)
      · −5.0% : fill 5% (1/50) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 59% si les 15 1res min sont vertes (91 cas) · 42% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 73% si début vert vs 27% si rouge (base 51% · écart 46 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **73%** · continue >prix actuel 48% ; creux résiduel méd -0.98% (q20 -1.94%) → **SL/trailing à −1.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.11% / q75 +2.25% → **scale +1.11% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **27%** (continue à baisser 55%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.35%** (au-delà de la MAE q10 -3.35%), cible rebond +1.38% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.13% .. +2.11%] · haut q95 +2.67% · bas q05 -3.59%
   - 60min (n=160) : retour [-3.4% .. +2.32%] · haut q95 +2.76% · bas q05 -3.88%
   - 2h (n=160) : retour [-2.3% .. +2.6%] · haut q95 +3.09% · bas q05 -4.41%
   - 4h (n=160) : retour [-2.73% .. +2.65%] · haut q95 +3.34% · bas q05 -5.82%
   - 6h (n=160) : retour [-2.75% .. +3.49%] · haut q95 +3.95% · bas q05 -7.35%
   - session (n=160) : retour [-3.79% .. +4.55%] · haut q95 +5.98% · bas q05 -7.35%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.26%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 25.5  _(survente)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -1.73  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 20.9%
- **ATR** : 11.68 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.089  _(distribution)_
- **Vol ratio** : 0.92  _(volume normal)_
- **Choppiness** : 50.3  _(transition)_
- **MA** : MA20 230.81 · MA50 231.06 · MA200 231.82  _(prix < MA20)_
- **Dist MA** : MA20 -5.6% · MA50 -5.7% · MA200 -6.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89430 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
