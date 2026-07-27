# 326030

**Generated** : 2026-07-27T21:55:38.983590+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩82000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩82000.00 (+0.4% vs entrée) · entrée ₩81685.56 · stop ₩80460.28 · T1 ₩83324.68 · R/R 1.34  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk -0.129 _(réel 5 s)_ (GBM -0.02) · ¼-Kelly 0.007 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩81371.12–₩82000.00 (mid ₩81685.56)
- Spot actuel : ₩82000.00 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : ₩80460.28 (stop swing_plan-based (-3.07%))
- Targets : T1 ₩83324.68 · R/R 1.34 | T2 ₩84963.80 · R/R 2.68 | T3 ₩86602.92 · R/R 4.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩80460.28


## Edge, scénarios & sizing

- EV/risk : -0.02 | EV/share : ₩-24.369 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 12 % | T3 6 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.6 | bear 5.3 | side 72.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.386% → cible +2.007% / stop −1.5%, p_fill 80%, n_eff≈37.9) : P(cible|rempli) **36%** · **EV/risk -0.129** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −0.845% → cible +4.487% / stop −2.243%, p_fill 85%, n_eff≈33.8) : P(cible|rempli) **16%** · **EV/risk -0.356** (×p_fill ; si rempli -0.94% du capital)
  - **deep** (entrée dip −1.247% → cible +6.345% / stop −3.173%, p_fill 91%, n_eff≈35.2) : P(cible|rempli) **17%** · **EV/risk -0.476** (×p_fill ; si rempli -1.66% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→45% · +3.0%→30% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.13% (p90 7.23%) · excursion haute méd. +1.65% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.676% vs midi 0.778% vs clôture 0.794% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑1%/↓2% ; spike-down 57% · recovery-V 19%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.101)_ ; drift intra méd. -0.206% ; recovery-V 21%
- **σ réalisé intraday** 3.381% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 61% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 80893.75 (VA 79843.75–81243.75 ; dernier close 80900.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 15% · rebond 81% · **stop −2.91%** sous le fill (sous le bruit) · cible +1.92% · R/R 0.66 (high win-rate)
- Gaps overnight (n=139) : méd. 0.1% · baisse 42% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=140) : bas méd −0.74% (p90 −2.25%) · haut méd +0.71% · range méd 1.99%
- Excursion ouverture 15min (n=140) : bas méd −0.83% (p90 −2.97%) · haut méd +0.82% · range méd 2.23%
- Excursion ouverture 30min (n=140) : bas méd −1.01% (p90 −3.02%) · haut méd +0.99% · range méd 2.56%
- Excursion ouverture 60min (n=140) : bas méd −1.17% (p90 −3.2%) · haut méd +1.34% · range méd 2.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 80900.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 79% (102/139) · gap 27% · délai 0.2min · rebond 51% (43/102) (MFE +1.19%)
   - −1.0% : fill 30min 54% · séance 68% (91/139) · gap 16% · délai 2.0min · rebond 54% (43/91) (MFE +1.01%)
   - −1.5% : fill 30min 40% · séance 54% (69/139) · gap 9% · délai 3.2min · rebond 58% (35/69) (MFE +1.22%)
   - −2.0% : fill 30min 27% · séance 46% (57/139) · gap 7% · délai 16.4min · rebond 64% (32/57) (MFE +1.43%)
   - −3.0% : fill 30min 10% · séance 33% (37/139) · gap 3% · délai 89.7min · rebond 56% (16/37) (MFE +1.32%)
   - −4.0% : fill 30min 7% · séance 21% (25/139) · gap 3% · délai 112.9min · rebond 54% (12/25) (MFE +1.03%)
   - −5.0% : fill 30min 6% · séance 15% (19/139) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.31% (p90 −2.16%) → stop au-delà de −1.14% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.54% (p90 −1.67%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.62%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=463 jambes) : jambe baissière méd −1.12% (p90 −2.43%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 94% (41/42) · rebond 66% (22/41)
      · −2.0% : fill 64% (28/42) · rebond 61% (14/28)
      · −3.0% : fill 42% (18/42) · rebond 49% (7/18)
      · −4.0% : fill 35% (15/42) · rebond 65% (8/15)
      · −5.0% : fill 28% (12/42) · rebond 85% (8/12)
   - **flat** (36 séances) :
      · −1.0% : fill 68% (25/36) · rebond 37% (9/25)
      · −2.0% : fill 54% (18/36) · rebond 74% (12/18)
      · −3.0% : fill 42% (11/36) · rebond 71% (6/11)
      · −4.0% : fill 30% (8/36) · rebond 39% (3/8)
      · −5.0% : fill 22% (6/36) · rebond 79% (4/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (25/61) · rebond 53% (12/25)
      · −2.0% : fill 26% (11/61) · rebond 56% (6/11)
      · −3.0% : fill 20% (8/61) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/61) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/61) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 40% en base · 70% si les 15 1res min sont vertes (52 cas) · 15% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=140) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 76% si début vert vs 6% si rouge (base 40% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **76%** · continue >prix actuel 40% ; creux résiduel méd -1.44% (q20 -2.38%) → **SL/trailing à −2.38%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +1.92% → **scale +1.23% / runner +1.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.0%** (au-delà de la MAE q10 -4.0%), cible rebond +0.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-2.77% .. +2.83%] · haut q95 +3.61% · bas q05 -4.02%
   - 60min (n=140) : retour [-3.78% .. +3.66%] · haut q95 +4.43% · bas q05 -4.41%
   - 2h (n=140) : retour [-3.46% .. +3.8%] · haut q95 +4.68% · bas q05 -4.58%
   - 4h (n=140) : retour [-3.95% .. +4.77%] · haut q95 +6.18% · bas q05 -5.72%
   - 6h (n=140) : retour [-4.54% .. +4.15%] · haut q95 +6.87% · bas q05 -5.94%
   - session (n=140) : retour [-4.65% .. +4.17%] · haut q95 +6.87% · bas q05 -5.94%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.6  _(neutre)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist 458.584  _(bullish_recent)_
- **BB** : %B 0.51 · largeur 20.8%
- **ATR** : 3971.43 (43.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.137  _(distribution)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 59.4  _(transition)_
- **MA** : MA20 81790.0 · MA50 86906.0 · MA200 106617.0  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 -5.6% · MA200 -23.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84119 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
