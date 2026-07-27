# 005930

**Generated** : 2026-07-27T21:49:11.990613+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩252500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩252500.00 (+2.8% vs entrée) · entrée ₩245625.00 · stop ₩236618.72 · T1 ₩263637.55 · R/R 2.0  
> ↳ P(T1 av. stop) 20 % _(réel 5 s)_ · EV/risk -0.323 _(réel 5 s)_ (GBM 0.559) · ¼-Kelly 0.029 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -33 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.220 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩242022.49–₩249227.51 (mid ₩245625.00)
- Spot actuel : ₩252500.00 (+2.8% au-dessus de la zone — repli à attendre)
- Stop : ₩236618.72 (stop swing_plan-based (-6.29%))
- Targets : T1 ₩263637.55 · R/R 2.0 | T2 ₩281650.11 · R/R 4.0 | T3 ₩299662.66 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩236618.72


## Edge, scénarios & sizing

- EV/risk : 0.559 | EV/share : ₩5032.032 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 15 % | T3 3 %
- Kelly (position) : f* 0.118 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 10.7 | bear 53.2 | side 36.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.234% → cible +5.063% / stop −2.72%, p_fill 80%, n_eff≈30.7) : P(cible|rempli) **14%** · **EV/risk -0.240** (×p_fill ; si rempli -0.81% du capital)
  - **swing** (entrée dip −2.723% → cible +7.333% / stop −3.667%, p_fill 74%, n_eff≈27.7) : P(cible|rempli) **20%** · **EV/risk -0.323** (×p_fill ; si rempli -1.61% du capital)
  - **deep** (entrée dip −4.213% → cible +10.371% / stop −5.185%, p_fill 68%, n_eff≈23.0) : P(cible|rempli) **10%** · **EV/risk -0.485** (×p_fill ; si rempli -3.70% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→66% · +2.0%→45% · +3.0%→30% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.45% (p90 9.05%) · excursion haute méd. +1.86% / basse méd. −2.52%
- Profil de vol intra : ouverture 2.779% vs midi 1.174% vs clôture 1.401% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 66% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.129 ; mean-reverting — autocorr -0.084)_ ; drift intra méd. -0.833% ; recovery-V 23%
- **σ réalisé intraday** 4.256% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 74% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 249681.25 (VA 247731.25–257481.25 ; dernier close 250000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 67% · **stop −6.06%** sous le fill (sous le bruit) · cible +1.51% · R/R 0.25 (high win-rate)
- Gaps overnight (n=139) : méd. 0.12% · baisse 46% (gap-down >1% 36% · >2% 24%)
- Excursion ouverture 5min (n=140) : bas méd −0.56% (p90 −1.47%) · haut méd +0.69% · range méd 1.41%
- Excursion ouverture 15min (n=140) : bas méd −0.88% (p90 −2.31%) · haut méd +1.05% · range méd 2.07%
- Excursion ouverture 30min (n=140) : bas méd −1.19% (p90 −2.79%) · haut méd +1.14% · range méd 2.47%
- Excursion ouverture 60min (n=140) : bas méd −1.52% (p90 −3.4%) · haut méd +1.36% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 250000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 54% · séance 66% (86/139) · gap 39% · délai 0.0min · rebond 53% (47/86) (MFE +1.4%)
   - −1.0% : fill 30min 50% · séance 63% (80/139) · gap 36% · délai 0.0min · rebond 60% (46/80) (MFE +1.39%)
   - −1.5% : fill 30min 44% · séance 56% (70/139) · gap 26% · délai 0.2min · rebond 58% (42/70) (MFE +1.64%)
   - −2.0% : fill 30min 41% · séance 50% (62/139) · gap 24% · délai 0.2min · rebond 57% (36/62) (MFE +1.77%)
   - −3.0% : fill 30min 32% · séance 45% (53/139) · gap 20% · délai 1.7min · rebond 61% (35/53) (MFE +2.05%)
   - −4.0% : fill 30min 24% · séance 38% (42/139) · gap 14% · délai 23.1min · rebond 63% (29/42) (MFE +2.09%)
   - −5.0% : fill 30min 13% · séance 30% (32/139) · gap 8% · délai 79.2min · rebond 67% (22/32) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −1.75%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −2.56%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.14%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=609 jambes) : jambe baissière méd −1.31% (p90 −3.07%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 97% (57/60) · rebond 50% (30/57)
      · −2.0% : fill 88% (49/60) · rebond 46% (25/49)
      · −3.0% : fill 86% (44/60) · rebond 55% (28/44)
      · −4.0% : fill 75% (36/60) · rebond 58% (24/36)
      · −5.0% : fill 64% (28/60) · rebond 63% (18/28)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (66 séances) :
      · −1.0% : fill 33% (16/66) · rebond 84% (12/16)
      · −2.0% : fill 18% (9/66) · rebond 94% (8/9)
      · −3.0% : fill 9% (5/66) · rebond 89% (4/5)
      · −4.0% : fill 8% (4/66) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/66) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 43% en base · 67% si les 15 1res min sont vertes (70 cas) · 18% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=140) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 82% si début vert vs 8% si rouge (base 43% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 129min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **82%** · continue >prix actuel 52% ; creux résiduel méd -1.59% (q20 -4.19%) → **SL/trailing à −4.19%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +3.38% → **scale +1.54% / runner +3.38%**, sortie à la clôture
  - **si ROUGE au coude** (n=64) : edge inversé — récupère vert seulement **8%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.23%** (au-delà de la MAE q10 -7.23%), cible rebond +0.93% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-2.64% .. +3.2%] · haut q95 +4.27% · bas q05 -3.09%
   - 60min (n=140) : retour [-3.02% .. +4.88%] · haut q95 +6.09% · bas q05 -3.64%
   - 2h (n=140) : retour [-4.29% .. +4.8%] · haut q95 +6.35% · bas q05 -5.12%
   - 4h (n=140) : retour [-6.1% .. +5.91%] · haut q95 +6.85% · bas q05 -7.27%
   - 6h (n=140) : retour [-6.46% .. +5.71%] · haut q95 +7.67% · bas q05 -7.92%
   - session (n=140) : retour [-6.11% .. +5.9%] · haut q95 +7.67% · bas q05 -8.65%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.3% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.75%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.6  _(momentum baissier)_
- **ADX** : 23.7  _(pas de tendance nette)_
- **MACD** : hist -2604.779  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 38.8%
- **ATR** : 22607.14 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.225  _(distribution)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 57.2  _(transition)_
- **MA** : MA20 280450.0 · MA50 303980.0 · MA200 190038.81  _(prix < MA20)_
- **Dist MA** : MA20 -10.0% · MA50 -16.9% · MA200 +32.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83603 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
