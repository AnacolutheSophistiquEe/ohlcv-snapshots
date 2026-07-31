# 326030

**Generated** : 2026-07-31T21:56:42.582374+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite normal · ₩79000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩79000.00 (+1.6% vs entrée) · entrée ₩77750.00 · stop ₩76225.00 · T1 ₩80800.00 · R/R 2.0  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.24 _(réel 5 s)_ (GBM -0.17) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.96% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

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

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩77487.21–₩78012.79 (mid ₩77750.00)
- Spot actuel : ₩79000.00 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : ₩76225.00 (stop swing_plan-based (-5.3%))
- Targets : T1 ₩80800.00 · R/R 2.0 | T2 ₩81239.97 · R/R 2.29 | T3 ₩81679.94 · R/R 2.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩76225.00


## Edge, scénarios & sizing

- EV/risk : -0.17 | EV/share : ₩-258.871 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 10 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 32.5 | bear 59.0 | side 8.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.58% → cible +3.923% / stop −1.961%, p_fill 56%, n_eff≈24.5) : P(cible|rempli) **7%** · **EV/risk -0.240** (×p_fill ; si rempli -0.84% du capital)
  - **swing** (entrée dip −3.482% → cible +3.767% / stop −1.884%, p_fill 47%, n_eff≈21.4) : P(cible|rempli) **35%** · **EV/risk +0.003** (×p_fill ; si rempli +0.01% du capital)
  - **deep** (entrée dip −5.379% → cible +5.328% / stop −2.664%, p_fill 57%, n_eff≈21.2) : P(cible|rempli) **36%** · **EV/risk +0.018** (×p_fill ; si rempli +0.08% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→45% · +3.0%→30% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.2% (p90 7.52%) · excursion haute méd. +1.62% / basse méd. −2.3%
- Profil de vol intra : ouverture 2.733% vs midi 0.826% vs clôture 0.829% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑1%/↓1% ; spike-down 58% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; mean-reverting — autocorr -0.104)_ ; drift intra méd. -0.451% ; recovery-V 23%
- **σ réalisé intraday** 3.461% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 75066.25 (VA 73858.75–77481.25 ; dernier close 75200.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 83% · **stop −2.8%** sous le fill (sous le bruit) · cible +1.82% · R/R 0.65 (high win-rate)
- Gaps overnight (n=142) : méd. 0.1% · baisse 42% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=143) : bas méd −0.77% (p90 −2.34%) · haut méd +0.68% · range méd 2.05%
- Excursion ouverture 15min (n=143) : bas méd −0.91% (p90 −2.96%) · haut méd +0.78% · range méd 2.28%
- Excursion ouverture 30min (n=143) : bas méd −1.08% (p90 −2.99%) · haut méd +1.07% · range méd 2.61%
- Excursion ouverture 60min (n=143) : bas méd −1.23% (p90 −3.18%) · haut méd +1.3% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 75200.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (105/142) · gap 27% · délai 0.3min · rebond 52% (45/105) (MFE +1.22%)
   - −1.0% : fill 30min 56% · séance 70% (94/142) · gap 17% · délai 1.6min · rebond 55% (45/94) (MFE +1.06%)
   - −1.5% : fill 30min 42% · séance 55% (71/142) · gap 9% · délai 1.8min · rebond 61% (37/71) (MFE +1.22%)
   - −2.0% : fill 30min 29% · séance 47% (59/142) · gap 6% · délai 10.7min · rebond 67% (34/59) (MFE +1.52%)
   - −3.0% : fill 30min 12% · séance 35% (39/142) · gap 3% · délai 90.0min · rebond 56% (17/39) (MFE +1.31%)
   - −4.0% : fill 30min 7% · séance 23% (27/142) · gap 3% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 5% · séance 16% (20/142) · gap 3% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.4% (p90 −2.63%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.61% (p90 −1.6%) → stop au-delà de −1.27% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.53% (p90 −1.62%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=482 jambes) : jambe baissière méd −1.13% (p90 −2.5%) · ~9.4 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 94% (42/43) · rebond 61% (22/42)
      · −2.0% : fill 66% (29/43) · rebond 65% (15/29)
      · −3.0% : fill 46% (19/43) · rebond 56% (8/19)
      · −4.0% : fill 39% (16/43) · rebond 70% (9/16)
      · −5.0% : fill 26% (12/43) · rebond 85% (8/12)
   - **flat** (38 séances) :
      · −1.0% : fill 71% (27/38) · rebond 47% (11/27)
      · −2.0% : fill 54% (19/38) · rebond 77% (13/19)
      · −3.0% : fill 43% (12/38) · rebond 61% (6/12)
      · −4.0% : fill 33% (9/38) · rebond 50% (4/9)
      · −5.0% : fill 25% (7/38) · rebond 84% (5/7)
   - **gap-up** (61 séances) :
      · −1.0% : fill 49% (25/61) · rebond 53% (12/25)
      · −2.0% : fill 26% (11/61) · rebond 56% (6/11)
      · −3.0% : fill 20% (8/61) · rebond 47% (3/8)
      · −4.0% : fill 3% (2/61) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/61) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 39% en base · 70% si les 15 1res min sont vertes (52 cas) · 17% si rouges (91 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=143) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 77% si début vert vs 6% si rouge (base 39% · écart 71 pts) ; prédictivité sature ensuite (plafond brut 202min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=59) : tient le vert **77%** · continue >prix actuel 38% ; creux résiduel méd -1.45% (q20 -2.36%) → **SL/trailing à −2.36%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.22% / q75 +1.92% → **scale +1.22% / runner +1.92%**, sortie à la clôture
  - **si ROUGE au coude** (n=84) : edge inversé — récupère vert seulement **6%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.05%** (au-delà de la MAE q10 -4.05%), cible rebond +0.75% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-2.76% .. +2.76%] · haut q95 +3.57% · bas q05 -3.93%
   - 60min (n=143) : retour [-3.72% .. +3.58%] · haut q95 +4.39% · bas q05 -4.29%
   - 2h (n=143) : retour [-3.4% .. +3.72%] · haut q95 +4.64% · bas q05 -4.5%
   - 4h (n=143) : retour [-4.45% .. +4.44%] · haut q95 +6.11% · bas q05 -6.0%
   - 6h (n=143) : retour [-5.37% .. +4.03%] · haut q95 +6.74% · bas q05 -6.48%
   - session (n=143) : retour [-5.11% .. +3.95%] · haut q95 +6.74% · bas q05 -6.54%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.38%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 44.6  _(momentum baissier)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist 305.154  _(pas de croisement recent)_
- **BB** : %B 0.43 · largeur 15.3%
- **ATR** : 4350.0 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.118  _(distribution)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 63.8  _(marche en range (choppy))_
- **MA** : MA20 79820.0 · MA50 85388.0 · MA200 106139.0  _(prix < MA20)_
- **Dist MA** : MA20 -1.0% · MA50 -7.5% · MA200 -25.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (83872 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
