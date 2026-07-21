# 005930

**Generated** : 2026-07-21T21:40:20.165461+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩259000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩259000.00 (+3.6% vs entrée) · entrée ₩249884.85 · stop ₩242095.56 · T1 ₩262000.00 · R/R 1.56  
> ↳ P(T1 av. stop) 4 % _(réel 5 s)_ · EV/risk -0.075 _(réel 5 s)_ (GBM -0.013) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.12% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


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

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩247977.49–₩251792.21 (mid ₩249884.85)
- Spot actuel : ₩259000.00 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : ₩242095.56 (stop swing_plan-based (-11.67%))
- Targets : T1 ₩262000.00 · R/R 1.56 | T2 ₩270204.28 · R/R 2.61 | T3 ₩278408.55 · R/R 3.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩242095.56


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : ₩-103.794 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 20 % | T3 20 %
- Kelly (position) : f* 0.038 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 62.3 | side 30.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.523% → cible +4.848% / stop −3.117%, p_fill 47%, n_eff≈16.2) : P(cible|rempli) **4%** · **EV/risk -0.075** (×p_fill ; si rempli -0.50% du capital)
  - **swing** (entrée dip −7.745% → cible +8.508% / stop −4.254%, p_fill 35%, n_eff≈11.4) : P(cible|rempli) **20%** · **EV/risk -0.141** (×p_fill ; si rempli -1.73% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→46% · +3.0%→30% · +5.0%→20% · +8.0%→5%
- Range intraday médian 5.38% (p90 9.32%) · excursion haute méd. +1.91% / basse méd. −2.45%
- Profil de vol intra : ouverture 2.748% vs midi 1.157% vs clôture 1.388% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (136 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑1%/↓1% ; spike-down 63% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.08)_ ; drift intra méd. -0.665% ; recovery-V 16%
- **σ réalisé intraday** 4.448% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 73% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 244006.25 (VA 241943.75–247306.25 ; dernier close 245500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 31% · rebond 71% · **stop −6.28%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.27 (high win-rate)
- Gaps overnight (n=135) : méd. 0.0% · baisse 48% (gap-down >1% 37% · >2% 26%)
- Excursion ouverture 5min (n=136) : bas méd −0.48% (p90 −1.48%) · haut méd +0.71% · range méd 1.42%
- Excursion ouverture 15min (n=136) : bas méd −0.88% (p90 −2.34%) · haut méd +1.05% · range méd 2.06%
- Excursion ouverture 30min (n=136) : bas méd −1.1% (p90 −2.73%) · haut méd +1.14% · range méd 2.47%
- Excursion ouverture 60min (n=136) : bas méd −1.38% (p90 −3.4%) · haut méd +1.36% · range méd 3.04%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 245500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 67% (84/135) · gap 40% · délai 0.0min · rebond 54% (46/84) (MFE +1.4%)
   - −1.0% : fill 30min 49% · séance 64% (78/135) · gap 37% · délai 0.0min · rebond 61% (45/78) (MFE +1.39%)
   - −1.5% : fill 30min 46% · séance 59% (69/135) · gap 28% · délai 0.3min · rebond 60% (42/69) (MFE +1.69%)
   - −2.0% : fill 30min 43% · séance 52% (61/135) · gap 26% · délai 0.0min · rebond 59% (36/61) (MFE +1.86%)
   - −3.0% : fill 30min 32% · séance 47% (52/135) · gap 21% · délai 0.9min · rebond 64% (35/52) (MFE +2.42%)
   - −4.0% : fill 30min 23% · séance 39% (41/135) · gap 15% · délai 16.7min · rebond 66% (29/41) (MFE +2.44%)
   - −5.0% : fill 30min 14% · séance 31% (31/135) · gap 9% · délai 61.2min · rebond 71% (22/31) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.32% (p90 −1.86%) → stop au-delà de −0.98% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.33% (p90 −2.6%) → stop au-delà de −1.06% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.29% (p90 −2.28%) → stop au-delà de −0.93% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=583 jambes) : jambe baissière méd −1.34% (p90 −3.08%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (59 séances) :
      · −1.0% : fill 97% (56/59) · rebond 52% (30/56)
      · −2.0% : fill 88% (48/59) · rebond 48% (25/48)
      · −3.0% : fill 85% (43/59) · rebond 58% (28/43)
      · −4.0% : fill 74% (35/59) · rebond 62% (24/35)
      · −5.0% : fill 62% (27/59) · rebond 68% (18/27)
   - **flat** (13 séances) :
      · −1.0% : fill 58% (7/13) · rebond 70% (4/7)
      · −2.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −3.0% : fill 40% (4/13) · rebond 85% (3/4)
      · −4.0% : fill 18% (2/13) · rebond 100% (2/2)
      · −5.0% : fill 18% (2/13) · rebond 100% (2/2)
   - **gap-up** (63 séances) :
      · −1.0% : fill 33% (15/63) · rebond 82% (11/15)
      · −2.0% : fill 20% (9/63) · rebond 94% (8/9)
      · −3.0% : fill 10% (5/63) · rebond 89% (4/5)
      · −4.0% : fill 10% (4/63) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/63) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=136) : 43% en base · 65% si les 15 1res min sont vertes (68 cas) · 20% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=136) : COUDE à **1:14** → P(séance verte=clôture>ouverture) 80% si début vert vs 9% si rouge (base 43% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 125min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **80%** · continue >prix actuel 52% ; creux résiduel méd -1.59% (q20 -4.36%) → **SL/trailing à −4.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +3.53% → **scale +1.54% / runner +3.53%**, sortie à la clôture
  - **si ROUGE au coude** (n=62) : edge inversé — récupère vert seulement **9%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.25%** (au-delà de la MAE q10 -7.25%), cible rebond +1.03% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=136) : retour [-2.28% .. +3.35%] · haut q95 +4.73% · bas q05 -3.09%
   - 60min (n=136) : retour [-3.05% .. +4.89%] · haut q95 +6.23% · bas q05 -3.73%
   - 2h (n=136) : retour [-4.53% .. +4.85%] · haut q95 +6.61% · bas q05 -5.13%
   - 4h (n=136) : retour [-5.33% .. +5.19%] · haut q95 +6.9% · bas q05 -7.48%
   - 6h (n=136) : retour [-6.59% .. +5.9%] · haut q95 +7.86% · bas q05 -8.19%
   - session (n=136) : retour [-5.96% .. +6.13%] · haut q95 +7.86% · bas q05 -8.97%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.72%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.0  _(momentum baissier)_
- **ADX** : 22.9  _(pas de tendance nette)_
- **MACD** : hist -6251.777  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 44.8%
- **ATR** : 25964.29 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.119  _(distribution)_
- **Vol ratio** : 0.64  _(volume normal)_
- **Choppiness** : 49.3  _(transition)_
- **MA** : MA20 296250.0 · MA50 305670.0 · MA200 186555.61  _(prix < MA20)_
- **Dist MA** : MA20 -12.6% · MA50 -15.3% · MA200 +38.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84372 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
