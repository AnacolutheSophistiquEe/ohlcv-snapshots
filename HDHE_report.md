# 267260

**Generated** : 2026-07-28T00:13:58.130143+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩797000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩797000.00 (+4.0% vs entrée) · entrée ₩766010.17 · stop ₩742450.85 · T1 ₩813128.81 · R/R 2.0  
> ↳ P(T1 av. stop) 16 % _(réel 5 s)_ · EV/risk -0.421 _(réel 5 s)_ (GBM 0.166) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩756586.44–₩775433.90 (mid ₩766010.17)
- Spot actuel : ₩797000.00 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : ₩742450.85 (stop swing_plan-based (-6.84%))
- Targets : T1 ₩813128.81 · R/R 2.0 | T2 ₩860247.44 · R/R 4.0 | T3 ₩907366.08 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩742450.85


## Edge, scénarios & sizing

- EV/risk : 0.166 | EV/share : ₩3912.370 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 17 % | T3 6 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 29.1 | bear 21.8 | side 49.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.772% → cible +6.369% / stop −8.0%, p_fill 81%, n_eff≈34.3) : P(cible|rempli) **10%** · **EV/risk -0.079** (×p_fill ; si rempli -0.78% du capital)
  - **swing** (entrée dip −3.884% → cible +6.151% / stop −3.076%, p_fill 78%, n_eff≈30.5) : P(cible|rempli) **16%** · **EV/risk -0.421** (×p_fill ; si rempli -1.66% du capital)
  - **deep** (entrée dip −6.012% → cible +8.699% / stop −4.35%, p_fill 79%, n_eff≈28.2) : P(cible|rempli) **24%** · **EV/risk -0.268** (×p_fill ; si rempli -1.48% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→48% · +3.0%→31% · +5.0%→11% · +8.0%→5%
- Range intraday médian 6.31% (p90 10.49%) · excursion haute méd. +1.85% / basse méd. −3.53%
- Profil de vol intra : ouverture 4.067% vs midi 1.081% vs clôture 1.152% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (140 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -1.439% ; recovery-V 19%
- **σ réalisé intraday** 4.698% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 71% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 806937.5 (VA 801312.5–825687.5 ; dernier close 811000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 85% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.03% · R/R 0.48 (high win-rate)
- Gaps overnight (n=139) : méd. 0.75% · baisse 39% (gap-down >1% 23% · >2% 10%)
- Excursion ouverture 5min (n=140) : bas méd −1.57% (p90 −3.71%) · haut méd +0.97% · range méd 2.7%
- Excursion ouverture 15min (n=140) : bas méd −1.79% (p90 −4.64%) · haut méd +1.06% · range méd 3.39%
- Excursion ouverture 30min (n=140) : bas méd −2.18% (p90 −4.86%) · haut méd +1.12% · range méd 3.77%
- Excursion ouverture 60min (n=140) : bas méd −2.56% (p90 −5.6%) · haut méd +1.33% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 811000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 71% (98/139) · gap 32% · délai 0.0min · rebond 52% (54/98) (MFE +1.07%)
   - −1.0% : fill 30min 55% · séance 68% (91/139) · gap 23% · délai 0.2min · rebond 54% (53/91) (MFE +1.02%)
   - −1.5% : fill 30min 48% · séance 62% (78/139) · gap 15% · délai 0.4min · rebond 67% (51/78) (MFE +1.28%)
   - −2.0% : fill 30min 44% · séance 58% (71/139) · gap 10% · délai 0.7min · rebond 68% (48/71) (MFE +1.78%)
   - −3.0% : fill 30min 33% · séance 49% (56/139) · gap 6% · délai 3.7min · rebond 78% (39/56) (MFE +1.89%)
   - −4.0% : fill 30min 23% · séance 43% (47/139) · gap 2% · délai 16.5min · rebond 76% (37/47) (MFE +2.29%)
   - −5.0% : fill 30min 14% · séance 36% (37/139) · gap 2% · délai 41.1min · rebond 85% (29/37) (MFE +2.03%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.72% (p90 −3.41%) → stop au-delà de −1.99% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −3.31%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −4.6%) → stop au-delà de −3.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=690 jambes) : jambe baissière méd −1.29% (p90 −3.58%) · ~11.1 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 98% (47/48) · rebond 49% (25/47)
      · −2.0% : fill 92% (40/48) · rebond 63% (24/40)
      · −3.0% : fill 82% (34/48) · rebond 78% (23/34)
      · −4.0% : fill 73% (30/48) · rebond 77% (24/30)
      · −5.0% : fill 62% (23/48) · rebond 86% (18/23)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (74 séances) :
      · −1.0% : fill 46% (30/74) · rebond 64% (21/30)
      · −2.0% : fill 33% (19/74) · rebond 71% (15/19)
      · −3.0% : fill 23% (11/74) · rebond 73% (8/11)
      · −4.0% : fill 21% (10/74) · rebond 82% (8/10)
      · −5.0% : fill 15% (7/74) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=140) : 34% en base · 50% si les 15 1res min sont vertes (66 cas) · 24% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=140) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 74% si début vert vs 10% si rouge (base 34% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **74%** · continue >prix actuel 45% ; creux résiduel méd -1.47% (q20 -3.65%) → **SL/trailing à −3.65%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +2.7% → **scale +1.23% / runner +2.7%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **10%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.17%** (au-delà de la MAE q10 -5.17%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=140) : retour [-5.08% .. +2.81%] · haut q95 +4.33% · bas q05 -5.61%
   - 60min (n=140) : retour [-5.56% .. +3.19%] · haut q95 +4.53% · bas q05 -6.01%
   - 2h (n=140) : retour [-6.84% .. +3.66%] · haut q95 +5.24% · bas q05 -7.37%
   - 4h (n=140) : retour [-6.94% .. +4.55%] · haut q95 +5.49% · bas q05 -8.26%
   - 6h (n=140) : retour [-6.9% .. +4.67%] · haut q95 +7.3% · bas q05 -8.81%
   - session (n=140) : retour [-6.97% .. +5.33%] · haut q95 +7.33% · bas q05 -9.03%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.7% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 37.1  _(momentum baissier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist 5071.517  _(bullish_recent)_
- **BB** : %B 0.31 · largeur 36.2%
- **ATR** : 62857.14 (71.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.054  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 857450.0 · MA50 977940.0 · MA200 920794.21  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -18.5% · MA200 -13.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83712 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
