# 267260

**Generated** : 2026-07-17T21:52:26.288429+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩797000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩797000.00 (+1.8% vs entrée) · entrée ₩782913.72 · stop ₩720280.62 · T1 ₩832775.15 · R/R 0.8  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.103 _(réel 5 s)_ (GBM -0.181) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

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

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩778953.11–₩786874.33 (mid ₩782913.72)
- Spot actuel : ₩797000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩720280.62 (stop swing_plan-based (-6.85%))
- Targets : T1 ₩832775.15 · R/R 0.8 | T2 ₩837458.97 · R/R 0.87 | T3 ₩842142.79 · R/R 0.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩720280.62


## Edge, scénarios & sizing

- EV/risk : -0.181 | EV/share : ₩-11313.103 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 9 % | T2 9 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 75.6 | side 17.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.772% → cible +6.369% / stop −8.0%, p_fill 86%, n_eff≈34.1) : P(cible|rempli) **7%** · **EV/risk -0.103** (×p_fill ; si rempli -0.95% du capital)
  - **swing** (entrée dip −3.89% → cible +5.639% / stop −3.08%, p_fill 81%, n_eff≈29.6) : P(cible|rempli) **27%** · **EV/risk -0.230** (×p_fill ; si rempli -0.87% du capital)
  - **deep** (entrée dip −6.013% → cible +7.974% / stop −3.987%, p_fill 71%, n_eff≈25.5) : P(cible|rempli) **25%** · **EV/risk -0.201** (×p_fill ; si rempli -1.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→66% · +2.0%→45% · +3.0%→29% · +5.0%→9% · +8.0%→5%
- Range intraday médian 5.91% (p90 10.49%) · excursion haute méd. +1.85% / basse méd. −3.42%
- Profil de vol intra : ouverture 3.947% vs midi 1.033% vs clôture 1.114% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (134 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.03)_ ; drift intra méd. -1.898% ; recovery-V 17%
- **σ réalisé intraday** 4.829% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 44% / bas 78% / whipsaw 25%
- POC intraday (dernière séance, temps-au-prix) : 797525.0 (VA 787025.0–797525.0 ; dernier close 796000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 82% · **stop −4.27%** sous le fill (sous le bruit) · cible +1.94% · R/R 0.45 (high win-rate)
- Gaps overnight (n=133) : méd. 0.76% · baisse 38% (gap-down >1% 22% · >2% 9%)
- Excursion ouverture 5min (n=134) : bas méd −1.57% (p90 −3.78%) · haut méd +0.9% · range méd 2.67%
- Excursion ouverture 15min (n=134) : bas méd −1.79% (p90 −4.69%) · haut méd +1.06% · range méd 3.32%
- Excursion ouverture 30min (n=134) : bas méd −2.18% (p90 −4.94%) · haut méd +1.07% · range méd 3.67%
- Excursion ouverture 60min (n=134) : bas méd −2.56% (p90 −5.65%) · haut méd +1.12% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 796000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (94/133) · gap 29% · délai 0.0min · rebond 52% (52/94) (MFE +1.08%)
   - −1.0% : fill 30min 55% · séance 68% (87/133) · gap 22% · délai 0.3min · rebond 52% (50/87) (MFE +1.01%)
   - −1.5% : fill 30min 48% · séance 61% (74/133) · gap 14% · délai 0.6min · rebond 66% (48/74) (MFE +1.27%)
   - −2.0% : fill 30min 43% · séance 57% (67/133) · gap 9% · délai 0.9min · rebond 67% (45/67) (MFE +1.61%)
   - −3.0% : fill 30min 31% · séance 49% (53/133) · gap 7% · délai 5.7min · rebond 75% (36/53) (MFE +1.58%)
   - −4.0% : fill 30min 22% · séance 42% (44/133) · gap 3% · délai 16.6min · rebond 78% (35/44) (MFE +2.23%)
   - −5.0% : fill 30min 12% · séance 34% (34/133) · gap 2% · délai 65.9min · rebond 82% (26/34) (MFE +1.94%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −3.32%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.91% (p90 −3.56%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.96% (p90 −5.2%) → stop au-delà de −3.39% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=644 jambes) : jambe baissière méd −1.34% (p90 −3.71%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 98% (44/45) · rebond 46% (23/44)
      · −2.0% : fill 90% (37/45) · rebond 62% (22/37)
      · −3.0% : fill 78% (31/45) · rebond 73% (20/31)
      · −4.0% : fill 67% (27/45) · rebond 80% (22/27)
      · −5.0% : fill 55% (20/45) · rebond 81% (15/20)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (71 séances) :
      · −1.0% : fill 47% (29/71) · rebond 61% (20/29)
      · −2.0% : fill 33% (18/71) · rebond 68% (14/18)
      · −3.0% : fill 26% (11/71) · rebond 73% (8/11)
      · −4.0% : fill 24% (10/71) · rebond 82% (8/10)
      · −5.0% : fill 17% (7/71) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=134) : 34% en base · 53% si les 15 1res min sont vertes (63 cas) · 22% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=134) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 75% si début vert vs 11% si rouge (base 34% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **75%** · continue >prix actuel 42% ; creux résiduel méd -1.63% (q20 -3.77%) → **SL/trailing à −3.77%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.21% / q75 +2.28% → **scale +1.21% / runner +2.28%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **11%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.31%** (au-delà de la MAE q10 -5.31%), cible rebond +1.65% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=134) : retour [-5.32% .. +3.02%] · haut q95 +4.42% · bas q05 -5.71%
   - 60min (n=134) : retour [-5.62% .. +3.36%] · haut q95 +4.64% · bas q05 -6.05%
   - 2h (n=134) : retour [-7.04% .. +3.68%] · haut q95 +5.84% · bas q05 -7.49%
   - 4h (n=134) : retour [-6.95% .. +3.34%] · haut q95 +5.58% · bas q05 -8.29%
   - 6h (n=134) : retour [-7.0% .. +4.27%] · haut q95 +7.72% · bas q05 -8.88%
   - session (n=134) : retour [-7.19% .. +3.94%] · haut q95 +7.72% · bas q05 -9.23%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.2  _(momentum baissier)_
- **ADX** : 22.6  _(pas de tendance nette)_
- **MACD** : hist -8710.452  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 37.5%
- **ATR** : 78642.86 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.222  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 45.9  _(transition)_
- **MA** : MA20 908900.0 · MA50 1045073.59 · MA200 914366.1  _(prix < MA20)_
- **Dist MA** : MA20 -12.3% · MA50 -23.7% · MA200 -12.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83611 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
