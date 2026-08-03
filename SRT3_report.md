# SRT3

**Generated** : 2026-08-03T00:02:04.342618+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · €219.80  

> 🟡 **WAIT-FOR-DIP** — spot +5.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €219.80 (+5.3% vs entrée) · entrée €208.69 · stop €205.21 · T1 €212.46 · R/R 1.08  
> ↳ P(T1 av. stop) 47 % · EV/risk 0.024 · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.67% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €207.93–€209.44 (mid €208.69)
- Spot actuel : €219.80 (+5.3% au-dessus de la zone — repli à attendre)
- Stop : €205.21 (stop swing_plan-based (-16.39%))
- Targets : T1 €212.46 · R/R 1.08 | T2 €216.24 · R/R 2.17 | T3 €220.02 · R/R 3.26
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €205.21


## Edge, scénarios & sizing

- EV/risk : 0.024 | EV/share : €0.082 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 17 % | T3 9 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.1 | bear 74.7 | side 10.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=5, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→76% · +2.0%→48% · +3.0%→26% · +5.0%→10% · +8.0%→0%
- Range intraday médian 3.63% (p90 7.16%) · excursion haute méd. +1.94% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.159% vs midi 0.919% vs clôture 1.037% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.111 ; neutre — autocorr 0.005)_ ; drift intra méd. -0.185% ; recovery-V 30%
- **σ réalisé intraday** 2.865% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 71% / bas 68% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 223.4712 (VA 223.1363–225.3138 ; dernier close 219.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 61% · rebond 72% · **stop −2.49%** sous le fill (sous le bruit) · cible +1.79% · R/R 0.72 (high win-rate)
- Gaps overnight (n=159) : méd. -0.04% · baisse 50% (gap-down >1% 16% · >2% 4%)
- Excursion ouverture 5min (n=160) : bas méd −0.41% (p90 −2.36%) · haut méd +0.57% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.57% (p90 −2.33%) · haut méd +0.66% · range méd 1.58%
- Excursion ouverture 30min (n=160) : bas méd −0.63% (p90 −2.76%) · haut méd +0.82% · range méd 1.76%
- Excursion ouverture 60min (n=160) : bas méd −0.74% (p90 −2.81%) · haut méd +0.89% · range méd 1.92%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 219.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 81% (127/159) · gap 30% · délai 0.2min · rebond 57% (66/127) (MFE +1.2%)
   - −1.0% : fill 30min 46% · séance 68% (106/159) · gap 16% · délai 0.6min · rebond 61% (63/106) (MFE +1.37%)
   - −1.5% : fill 30min 38% · séance 61% (93/159) · gap 7% · délai 4.4min · rebond 72% (60/93) (MFE +1.79%)
   - −2.0% : fill 30min 23% · séance 43% (72/159) · gap 4% · délai 17.5min · rebond 63% (44/72) (MFE +1.96%)
   - −3.0% : fill 30min 7% · séance 21% (40/159) · gap 1% · délai 138.5min · rebond 57% (23/40) (MFE +1.67%)
   - −4.0% : fill 30min 4% · séance 12% (21/159) · gap 1% · délai 49.4min · rebond 76% (16/21) (MFE +2.62%)
   - −5.0% : fill 30min 1% · séance 8% (12/159) · gap 1% · délai 94.0min · rebond 65% (9/12) (MFE +2.48%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.49% (p90 −2.35%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.2% (p90 −2.43%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.59% (p90 −2.8%) → stop au-delà de −2.04% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=428 jambes) : jambe baissière méd −1.04% (p90 −2.7%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (74 séances) :
      · −1.0% : fill 86% (62/74) · rebond 68% (41/62)
      · −2.0% : fill 54% (42/74) · rebond 64% (27/42)
      · −3.0% : fill 32% (28/74) · rebond 48% (15/28)
      · −4.0% : fill 15% (15/74) · rebond 71% (11/15)
      · −5.0% : fill 8% (7/74) · rebond 92% (6/7)
   - **flat** (34 séances) :
      · −1.0% : fill 59% (19/34) · rebond 50% (9/19)
      · −2.0% : fill 49% (15/34) · rebond 55% (7/15)
      · −3.0% : fill 20% (6/34) · rebond 66% (4/6)
      · −4.0% : fill 15% (4/34) · rebond 70% (3/4)
      · −5.0% : fill 15% (4/34) · rebond 24% (2/4)
   - **gap-up** (51 séances) :
      · −1.0% : fill 55% (25/51) · rebond 55% (13/25)
      · −2.0% : fill 25% (15/51) · rebond 72% (10/15)
      · −3.0% : fill 9% (6/51) · rebond 78% (4/6)
      · −4.0% : fill 6% (2/51) · rebond 100% (2/2)
      · −5.0% : fill 5% (1/51) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 55% si les 15 1res min sont vertes (91 cas) · 42% si rouges (69 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **3:25** → P(séance verte=clôture>ouverture) 70% si début vert vs 26% si rouge (base 49% · écart 44 pts) ; prédictivité sature ensuite (plafond brut 293min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **70%** · continue >prix actuel 47% ; creux résiduel méd -1.05% (q20 -1.96%) → **SL/trailing à −1.96%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.06% / q75 +2.2% → **scale +1.06% / runner +2.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **26%** (continue à baisser 57%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.35%** (au-delà de la MAE q10 -3.35%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.1% .. +2.11%] · haut q95 +2.66% · bas q05 -3.58%
   - 60min (n=160) : retour [-3.36% .. +2.31%] · haut q95 +2.72% · bas q05 -3.87%
   - 2h (n=160) : retour [-2.26% .. +2.59%] · haut q95 +3.06% · bas q05 -4.25%
   - 4h (n=160) : retour [-2.71% .. +2.56%] · haut q95 +3.33% · bas q05 -5.6%
   - 6h (n=160) : retour [-2.73% .. +3.41%] · haut q95 +3.89% · bas q05 -7.25%
   - session (n=160) : retour [-3.77% .. +4.44%] · haut q95 +5.9% · bas q05 -7.25%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.27%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 26.2  _(survente)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist -1.615  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 20.7%
- **ATR** : 11.59 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.052  _(distribution)_
- **Vol ratio** : 0.17  _(volume atone)_
- **Choppiness** : 50.0  _(transition)_
- **MA** : MA20 230.9 · MA50 231.1 · MA200 231.83  _(prix < MA20)_
- **Dist MA** : MA20 -4.8% · MA50 -4.9% · MA200 -5.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89501 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
