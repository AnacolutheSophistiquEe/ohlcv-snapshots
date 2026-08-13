# PRY

**Generated** : 2026-08-13T00:11:14.512135+00:00  
**Santé technique** : 9/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €132.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €132.00 (+1.7% vs entrée) · entrée €129.80 · stop €119.42 · T1 €131.77 · R/R 0.19  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.037 _(réel 5 s)_ (GBM -0.046) · ¼-Kelly 0.092 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 9/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €129.41–€130.19 (mid €129.80)
- Spot actuel : €132.00 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €119.42 (stop swing_plan-based (-8.52%))
- Targets : T1 €131.77 · R/R 0.19 | T2 €133.74 · R/R 0.38 | T3 €135.71 · R/R 0.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €119.42


## Edge, scénarios & sizing

- EV/risk : -0.046 | EV/share : €-0.475 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 28 % | T3 11 %
- Kelly (position) : f* 0.368 | ¼-Kelly 0.092 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 27.1 | bear 59.7 | side 13.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 396.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.663% → cible +1.517% / stop −8.0%, p_fill 52%, n_eff≈21.9) : P(cible|rempli) **37%** · **EV/risk -0.037** (×p_fill ; si rempli -0.57% du capital)
  - **swing** (entrée dip −3.663% → cible +3.392% / stop −5.041%, p_fill 59%, n_eff≈20.4) : P(cible|rempli) **59%** · **EV/risk -0.006** (×p_fill ; si rempli -0.05% du capital)
  - **deep** (entrée dip −5.665% → cible +4.797% / stop −7.723%, p_fill 49%, n_eff≈17.3) : P(cible|rempli) **43%** · **EV/risk -0.123** (×p_fill ; si rempli -1.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→68% · +2.0%→42% · +3.0%→29% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.35% (p90 6.51%) · excursion haute méd. +1.63% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.454% vs midi 0.865% vs clôture 1.2% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; neutre — autocorr -0.007)_ ; drift intra méd. -0.779% ; recovery-V 30%
- **σ réalisé intraday** 2.824% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 62% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 128.2262 (VA 127.1513–129.3012 ; dernier close 127.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=151) : méd. 0.39% · baisse 39% (gap-down >1% 19% · >2% 10%)
- Excursion ouverture 5min (n=152) : bas méd −0.88% (p90 −2.3%) · haut méd +0.35% · range méd 1.42%
- Excursion ouverture 15min (n=152) : bas méd −1.03% (p90 −2.87%) · haut méd +0.53% · range méd 1.77%
- Excursion ouverture 30min (n=152) : bas méd −1.04% (p90 −3.16%) · haut méd +0.66% · range méd 1.93%
- Excursion ouverture 60min (n=152) : bas méd −1.21% (p90 −3.32%) · haut méd +0.86% · range méd 2.21%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 127.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 70% (109/151) · gap 25% · délai 0.2min · rebond 63% (69/109) (MFE +1.34%)
   - −1.0% : fill 30min 47% · séance 61% (92/151) · gap 19% · délai 0.3min · rebond 61% (56/92) (MFE +1.57%)
   - −1.5% : fill 30min 33% · séance 53% (80/151) · gap 15% · délai 2.0min · rebond 53% (44/80) (MFE +1.14%)
   - −2.0% : fill 30min 24% · séance 44% (65/151) · gap 10% · délai 5.4min · rebond 61% (41/65) (MFE +1.34%)
   - −3.0% : fill 30min 13% · séance 34% (47/151) · gap 4% · délai 76.9min · rebond 65% (32/47) (MFE +1.64%)
   - −4.0% : fill 30min 3% · séance 20% (25/151) · gap 1% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 1% · séance 13% (17/151) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −1.97%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.05%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −2.02%) → stop au-delà de −1.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=478 jambes) : jambe baissière méd −1.06% (p90 −2.59%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 90% (47/52) · rebond 46% (26/47)
      · −2.0% : fill 73% (38/52) · rebond 64% (26/38)
      · −3.0% : fill 60% (29/52) · rebond 71% (22/29)
      · −4.0% : fill 38% (16/52) · rebond 65% (11/16)
      · −5.0% : fill 29% (12/52) · rebond 73% (9/12)
   - **flat** (27 séances) :
      · −1.0% : fill 69% (15/27) · rebond 71% (10/15)
      · −2.0% : fill 45% (8/27) · rebond 86% (6/8)
      · −3.0% : fill 22% (5/27) · rebond 40% (2/5)
      · −4.0% : fill 10% (3/27) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/27) · rebond 25% (1/2)
   - **gap-up** (72 séances) :
      · −1.0% : fill 42% (30/72) · rebond 74% (20/30)
      · −2.0% : fill 27% (19/72) · rebond 43% (9/19)
      · −3.0% : fill 21% (13/72) · rebond 63% (8/13)
      · −4.0% : fill 11% (6/72) · rebond 86% (5/6)
      · −5.0% : fill 5% (3/72) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 48% en base · 67% si les 15 1res min sont vertes (70 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=152) : COUDE à **1:07** → P(séance verte=clôture>ouverture) 79% si début vert vs 26% si rouge (base 48% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **79%** · continue >prix actuel 63% ; creux résiduel méd -1.32% (q20 -2.07%) → **SL/trailing à −2.07%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.52% / q75 +2.54% → **scale +1.52% / runner +2.54%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **26%** (continue à baisser 62%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.3%** (au-delà de la MAE q10 -4.3%), cible rebond +1.21% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-2.93% .. +2.75%] · haut q95 +3.46% · bas q05 -3.4%
   - 60min (n=152) : retour [-3.39% .. +2.2%] · haut q95 +3.94% · bas q05 -3.58%
   - 2h (n=152) : retour [-3.63% .. +2.41%] · haut q95 +4.09% · bas q05 -4.74%
   - 4h (n=152) : retour [-3.65% .. +3.2%] · haut q95 +4.37% · bas q05 -4.89%
   - 6h (n=152) : retour [-3.73% .. +3.66%] · haut q95 +4.64% · bas q05 -5.42%
   - session (n=152) : retour [-4.46% .. +4.14%] · haut q95 +5.51% · bas q05 -6.32%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.6% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 55.1  _(momentum haussier)_
- **ADX** : 29.9  _(tendance etablie)_
- **MACD** : hist 1.61  _(pas de croisement recent)_
- **BB** : %B 0.84 · largeur 16.0%
- **ATR** : 6.41 (94.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.069  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 49.0  _(transition)_
- **MA** : MA20 125.11 · MA50 136.46 · MA200 111.75  _(prix > MA20)_
- **Dist MA** : MA20 +5.5% · MA50 -3.3% · MA200 +18.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94287 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
