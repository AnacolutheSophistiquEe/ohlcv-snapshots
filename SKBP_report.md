# 326030

**Generated** : 2026-07-29T21:55:52.602072+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · ₩75000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)  
> ↳ spot ₩75000.00 (+0.7% vs entrée) · entrée ₩74449.57 · stop ₩73076.61 · T1 ₩77195.49 · R/R 2.0  
> ↳ P(T1 av. stop) 30 % _(réel 5 s)_ · EV/risk -0.156 _(réel 5 s)_ (GBM -0.092) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩73900.39–₩74998.76 (mid ₩74449.57)
- Spot actuel : ₩75000.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩73076.61 (stop swing_plan-based (-2.56%))
- Targets : T1 ₩77195.49 · R/R 2.0 | T2 ₩79941.41 · R/R 4.0 | T3 ₩82687.33 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩73076.61


## Edge, scénarios & sizing

- EV/risk : -0.092 | EV/share : ₩-125.742 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 45.2 | bear 33.1 | side 21.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.336% → cible +1.649% / stop −1.68%, p_fill 84%, n_eff≈37.9) : P(cible|rempli) **47%** · **EV/risk -0.081** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −0.729% → cible +3.688% / stop −1.844%, p_fill 84%, n_eff≈35.1) : P(cible|rempli) **30%** · **EV/risk -0.156** (×p_fill ; si rempli -0.34% du capital)
  - **deep** (entrée dip −1.131% → cible +5.216% / stop −2.608%, p_fill 88%, n_eff≈35.8) : P(cible|rempli) **17%** · **EV/risk -0.463** (×p_fill ; si rempli -1.38% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→45% · +3.0%→30% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.2% (p90 7.23%) · excursion haute méd. +1.62% / basse méd. −2.18%
- Profil de vol intra : ouverture 2.711% vs midi 0.8% vs clôture 0.818% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (142 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑1%/↓1% ; spike-down 57% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.101)_ ; drift intra méd. -0.204% ; recovery-V 25%
- **σ réalisé intraday** 3.352% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 60% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 79531.25 (VA 79181.25–81456.25 ; dernier close 79500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −3.7%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.41 (high win-rate)
- Gaps overnight (n=141) : méd. 0.0% · baisse 42% (gap-down >1% 18% · >2% 6%)
- Excursion ouverture 5min (n=142) : bas méd −0.77% (p90 −2.21%) · haut méd +0.72% · range méd 1.99%
- Excursion ouverture 15min (n=142) : bas méd −0.88% (p90 −2.96%) · haut méd +0.82% · range méd 2.23%
- Excursion ouverture 30min (n=142) : bas méd −1.05% (p90 −2.99%) · haut méd +1.12% · range méd 2.6%
- Excursion ouverture 60min (n=142) : bas méd −1.22% (p90 −3.19%) · haut méd +1.34% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 79500.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (104/141) · gap 28% · délai 0.2min · rebond 51% (44/104) (MFE +1.19%)
   - −1.0% : fill 30min 55% · séance 69% (93/141) · gap 18% · délai 1.6min · rebond 54% (44/93) (MFE +1.01%)
   - −1.5% : fill 30min 40% · séance 54% (70/141) · gap 9% · délai 2.3min · rebond 60% (36/70) (MFE +1.17%)
   - −2.0% : fill 30min 28% · séance 46% (58/141) · gap 6% · délai 14.3min · rebond 66% (33/58) (MFE +1.5%)
   - −3.0% : fill 30min 12% · séance 34% (38/141) · gap 3% · délai 81.3min · rebond 59% (17/38) (MFE +1.39%)
   - −4.0% : fill 30min 7% · séance 22% (26/141) · gap 3% · délai 131.3min · rebond 58% (13/26) (MFE +1.26%)
   - −5.0% : fill 30min 6% · séance 14% (19/141) · gap 3% · délai 118.4min · rebond 81% (12/19) (MFE +1.92%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.0%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −1.6%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.62%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=474 jambes) : jambe baissière méd −1.11% (p90 −2.43%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 94% (42/43) · rebond 61% (22/42)
      · −2.0% : fill 66% (29/43) · rebond 65% (15/29)
      · −3.0% : fill 46% (19/43) · rebond 56% (8/19)
      · −4.0% : fill 39% (16/43) · rebond 70% (9/16)
      · −5.0% : fill 26% (12/43) · rebond 85% (8/12)
   - **flat** (37 séances) :
      · −1.0% : fill 70% (26/37) · rebond 42% (10/26)
      · −2.0% : fill 51% (18/37) · rebond 74% (12/18)
      · −3.0% : fill 39% (11/37) · rebond 71% (6/11)
      · −4.0% : fill 28% (8/37) · rebond 39% (3/8)
      · −5.0% : fill 20% (6/37) · rebond 79% (4/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (25/61) · rebond 53% (12/25)
      · −2.0% : fill 26% (11/61) · rebond 56% (6/11)
      · −3.0% : fill 20% (8/61) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/61) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/61) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=142) : 40% en base · 70% si les 15 1res min sont vertes (52 cas) · 17% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=142) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 77% si début vert vs 6% si rouge (base 40% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 202min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **77%** · continue >prix actuel 38% ; creux résiduel méd -1.45% (q20 -2.36%) → **SL/trailing à −2.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.22% / q75 +1.92% → **scale +1.22% / runner +1.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **6%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.97%** (au-delà de la MAE q10 -3.97%), cible rebond +0.78% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=142) : retour [-2.76% .. +2.78%] · haut q95 +3.58% · bas q05 -3.96%
   - 60min (n=142) : retour [-3.75% .. +3.61%] · haut q95 +4.4% · bas q05 -4.35%
   - 2h (n=142) : retour [-3.42% .. +3.75%] · haut q95 +4.65% · bas q05 -4.53%
   - 4h (n=142) : retour [-3.82% .. +4.55%] · haut q95 +6.14% · bas q05 -5.69%
   - 6h (n=142) : retour [-4.53% .. +4.07%] · haut q95 +6.78% · bas q05 -5.91%
   - session (n=142) : retour [-4.64% .. +3.96%] · haut q95 +6.78% · bas q05 -5.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.2  _(momentum baissier)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist 183.203  _(bullish_recent)_
- **BB** : %B 0.12 · largeur 18.3%
- **ATR** : 4185.71 (52.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.215  _(distribution)_
- **Vol ratio** : 1.19  _(volume normal)_
- **Choppiness** : 64.1  _(marche en range (choppy))_
- **MA** : MA20 80625.0 · MA50 86014.0 · MA200 106376.0  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -12.8% · MA200 -29.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83905 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
