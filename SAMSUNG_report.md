# 005930

**Generated** : 2026-07-22T21:49:41.099996+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩260500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩260500.00 (+3.8% vs entrée) · entrée ₩251009.85 · stop ₩243445.56 · T1 ₩262000.00 · R/R 1.45  
> ↳ P(T1 av. stop) 5 % _(réel 5 s)_ · EV/risk -0.06 _(réel 5 s)_ (GBM 0.005) · ¼-Kelly 0.009 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.01% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


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

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩249245.27–₩252774.42 (mid ₩251009.85)
- Spot actuel : ₩260500.00 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : ₩243445.56 (stop swing_plan-based (-11.62%))
- Targets : T1 ₩262000.00 · R/R 1.45 | T2 ₩269699.14 · R/R 2.47 | T3 ₩277398.28 · R/R 3.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩243445.56


## Edge, scénarios & sizing

- EV/risk : 0.005 | EV/share : ₩37.102 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.037 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 62.3 | side 30.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.646% → cible +4.378% / stop −3.014%, p_fill 45%, n_eff≈16.2) : P(cible|rempli) **5%** · **EV/risk -0.060** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −8.016% → cible +7.836% / stop −3.918%, p_fill 38%, n_eff≈12.1) : P(cible|rempli) **18%** · **EV/risk -0.179** (×p_fill ; si rempli -1.87% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=8, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→46% · +3.0%→31% · +5.0%→21% · +8.0%→5%
- Range intraday médian 5.45% (p90 9.32%) · excursion haute méd. +1.91% / basse méd. −2.45%
- Profil de vol intra : ouverture 2.759% vs midi 1.159% vs clôture 1.386% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 11% · trend ↑1%/↓1% ; spike-down 63% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.082)_ ; drift intra méd. -0.39% ; recovery-V 21%
- **σ réalisé intraday** 4.407% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 70% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 259143.75 (VA 256581.25–263243.75 ; dernier close 260000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 30% · rebond 71% · **stop −6.28%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.27 (high win-rate)
- Gaps overnight (n=136) : méd. 0.04% · baisse 47% (gap-down >1% 36% · >2% 26%)
- Excursion ouverture 5min (n=137) : bas méd −0.51% (p90 −1.48%) · haut méd +0.71% · range méd 1.5%
- Excursion ouverture 15min (n=137) : bas méd −0.88% (p90 −2.33%) · haut méd +1.07% · range méd 2.07%
- Excursion ouverture 30min (n=137) : bas méd −1.15% (p90 −2.72%) · haut méd +1.17% · range méd 2.47%
- Excursion ouverture 60min (n=137) : bas méd −1.46% (p90 −3.4%) · haut méd +1.37% · range méd 3.05%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 260000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 68% (85/136) · gap 39% · délai 0.0min · rebond 55% (47/85) (MFE +1.51%)
   - −1.0% : fill 30min 50% · séance 65% (79/136) · gap 36% · délai 0.0min · rebond 62% (46/79) (MFE +1.48%)
   - −1.5% : fill 30min 45% · séance 58% (69/136) · gap 28% · délai 0.3min · rebond 60% (42/69) (MFE +1.69%)
   - −2.0% : fill 30min 42% · séance 51% (61/136) · gap 26% · délai 0.0min · rebond 59% (36/61) (MFE +1.86%)
   - −3.0% : fill 30min 32% · séance 46% (52/136) · gap 21% · délai 0.9min · rebond 64% (35/52) (MFE +2.42%)
   - −4.0% : fill 30min 23% · séance 38% (41/136) · gap 15% · délai 16.7min · rebond 66% (29/41) (MFE +2.44%)
   - −5.0% : fill 30min 14% · séance 30% (31/136) · gap 9% · délai 61.2min · rebond 71% (22/31) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.33% (p90 −1.76%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.38% (p90 −2.56%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −2.14%) → stop au-delà de −1.12% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=589 jambes) : jambe baissière méd −1.32% (p90 −3.07%) · ~12.0 jambes/séance
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
   - **gap-up** (64 séances) :
      · −1.0% : fill 36% (16/64) · rebond 84% (12/16)
      · −2.0% : fill 19% (9/64) · rebond 94% (8/9)
      · −3.0% : fill 10% (5/64) · rebond 89% (4/5)
      · −4.0% : fill 9% (4/64) · rebond 88% (3/4)
      · −5.0% : fill 3% (2/64) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 44% en base · 66% si les 15 1res min sont vertes (69 cas) · 20% si rouges (68 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=137) : COUDE à **27min** → P(séance verte=clôture>ouverture) 78% si début vert vs 11% si rouge (base 44% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 125min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **78%** · continue >prix actuel 63% ; creux résiduel méd -1.61% (q20 -4.63%) → **SL/trailing à −4.63%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.45% / q75 +4.41% → **scale +2.45% / runner +4.41%**, sortie à la clôture
  - **si ROUGE au coude** (n=67) : edge inversé — récupère vert seulement **11%** (continue à baisser 63%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.82%** (au-delà de la MAE q10 -6.82%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-2.28% .. +3.33%] · haut q95 +4.62% · bas q05 -3.09%
   - 60min (n=137) : retour [-3.05% .. +4.89%] · haut q95 +6.22% · bas q05 -3.71%
   - 2h (n=137) : retour [-4.47% .. +4.85%] · haut q95 +6.53% · bas q05 -5.13%
   - 4h (n=137) : retour [-5.32% .. +6.0%] · haut q95 +6.89% · bas q05 -7.42%
   - 6h (n=137) : retour [-6.54% .. +5.8%] · haut q95 +7.82% · bas q05 -8.12%
   - session (n=137) : retour [-5.88% .. +5.94%] · haut q95 +7.82% · bas q05 -8.89%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 005930 = **volatil sans tendance propre (choppy)** (vol intra méd 2.73%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.5  _(momentum baissier)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist -4968.409  _(pas de croisement recent)_
- **BB** : %B 0.25 · largeur 46.2%
- **ATR** : 25214.29 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.09  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 54.0  _(transition)_
- **MA** : MA20 293775.0 · MA50 305510.0 · MA200 187445.33  _(prix < MA20)_
- **Dist MA** : MA20 -11.3% · MA50 -14.7% · MA200 +39.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84756 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
