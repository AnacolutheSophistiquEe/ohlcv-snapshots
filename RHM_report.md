# RHM

**Generated** : 2026-07-09T21:36:11.204731+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €1013.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €1013.20 (+2.1% vs entrée) · entrée €992.10 · stop €972.26 · T1 €1022.35 · R/R 1.52  
> ↳ P(T1 av. stop) 9 % _(réel 5 s)_ · EV/risk -0.229 _(réel 5 s)_ (GBM 0.003) · ¼-Kelly 0.004 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.140 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €986.05–€998.15 (mid €992.10)
- Spot actuel : €1013.20 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : €972.26 (stop swing_plan-based (-7.83%))
- Targets : T1 €1022.35 · R/R 1.52 | T2 €1052.61 · R/R 3.05 | T3 €1082.86 · R/R 4.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €972.26


## Edge, scénarios & sizing

- EV/risk : 0.003 | EV/share : €0.068 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.015 | ¼-Kelly 0.004 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 26.1 | bear 5.0 | side 68.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.082% → cible +3.05% / stop −2.0%, p_fill 38%, n_eff≈13.4) : P(cible|rempli) **9%** · **EV/risk -0.229** (×p_fill ; si rempli -1.22% du capital)
  - **swing** (entrée dip −4.577% → cible +6.819% / stop −3.41%, p_fill 25%, n_eff≈12.2) : P(cible|rempli) **4%** · **EV/risk -0.163** (×p_fill ; si rempli -2.19% du capital)
  - **deep** (entrée dip −7.08% → cible +9.644% / stop −4.822%, p_fill 33%, n_eff≈11.4) : P(cible|rempli) **7%** · **EV/risk -0.188** (×p_fill ; si rempli -2.78% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→49% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.65%) · excursion haute méd. +1.98% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.567% vs midi 0.9% vs clôture 1.018% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; neutre — autocorr 0.023)_ ; drift intra méd. -0.36% ; recovery-V 40%
- **σ réalisé intraday** 2.86% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1064.385 (VA 1062.695–1076.215 ; dernier close 1063.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 59% · **stop −3.66%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 41% (gap-down >1% 15% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −1.54%) · haut méd +0.57% · range méd 1.43%
- Excursion ouverture 15min (n=160) : bas méd −1.0% (p90 −2.0%) · haut méd +0.74% · range méd 1.97%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −2.24%) · haut méd +0.95% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.1% (p90 −2.57%) · haut méd +1.01% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1063.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 76% (120/159) · gap 27% · délai 0.3min · rebond 58% (63/120) (MFE +1.24%)
   - −1.0% : fill 30min 47% · séance 70% (107/159) · gap 15% · délai 5.6min · rebond 62% (62/107) (MFE +1.42%)
   - −1.5% : fill 30min 30% · séance 55% (80/159) · gap 8% · délai 18.2min · rebond 51% (42/80) (MFE +1.14%)
   - −2.0% : fill 30min 23% · séance 45% (69/159) · gap 6% · délai 27.5min · rebond 65% (41/69) (MFE +1.34%)
   - −3.0% : fill 30min 10% · séance 29% (45/159) · gap 3% · délai 118.7min · rebond 63% (29/45) (MFE +1.48%)
   - −4.0% : fill 30min 4% · séance 21% (27/159) · gap 2% · délai 203.8min · rebond 59% (16/27) (MFE +1.47%)
   - −5.0% : fill 30min 2% · séance 11% (15/159) · gap 2% · délai 157.4min · rebond 56% (8/15) (MFE +1.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −1.52%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −1.68%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −1.64%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.1% (p90 −2.58%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 92% (47/49) · rebond 62% (25/47)
      · −2.0% : fill 77% (37/49) · rebond 67% (24/37)
      · −3.0% : fill 47% (26/49) · rebond 57% (17/26)
      · −4.0% : fill 36% (15/49) · rebond 61% (10/15)
      · −5.0% : fill 22% (9/49) · rebond 77% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 79% (37/50) · rebond 67% (24/37)
      · −2.0% : fill 36% (18/50) · rebond 71% (10/18)
      · −3.0% : fill 24% (11/50) · rebond 56% (6/11)
      · −4.0% : fill 22% (9/50) · rebond 38% (3/9)
      · −5.0% : fill 14% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 45% (23/60) · rebond 55% (13/23)
      · −2.0% : fill 26% (14/60) · rebond 54% (7/14)
      · −3.0% : fill 18% (8/60) · rebond 83% (6/8)
      · −4.0% : fill 8% (3/60) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/60) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 49% en base · 67% si les 15 1res min sont vertes (84 cas) · 32% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 79% si début vert vs 24% si rouge (base 49% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=76) : tient le vert **79%** · continue >prix actuel 48% ; creux résiduel méd -1.37% (q20 -2.37%) → **SL/trailing à −2.37%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.87% → **scale +1.19% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **24%** (continue à baisser 54%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.0%** (au-delà de la MAE q10 -5.0%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +3.14%] · haut q95 +3.84% · bas q05 -3.0%
   - 60min (n=160) : retour [-3.06% .. +3.11%] · haut q95 +4.06% · bas q05 -3.67%
   - 2h (n=160) : retour [-3.42% .. +2.89%] · haut q95 +4.16% · bas q05 -4.4%
   - 4h (n=160) : retour [-3.29% .. +3.03%] · haut q95 +4.54% · bas q05 -4.98%
   - 6h (n=160) : retour [-4.37% .. +3.52%] · haut q95 +4.54% · bas q05 -5.58%
   - session (n=160) : retour [-6.15% .. +4.27%] · haut q95 +4.77% · bas q05 -6.93%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.27%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.2  _(momentum baissier)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist 5.894  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 33.5%
- **ATR** : 63.76 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.139  _(distribution)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 40.7  _(transition)_
- **MA** : MA20 1089.37 · MA50 1175.17 · MA200 1529.44  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -13.8% · MA200 -33.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92272 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
