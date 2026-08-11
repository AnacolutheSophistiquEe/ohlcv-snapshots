# NEX

**Generated** : 2026-08-11T00:08:17.718376+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €138.60  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €138.60 (+5.9% vs entrée) · entrée €130.88 · stop €125.82 · T1 €134.25 · R/R 0.67  
> ↳ P(T1 av. stop) 75 % · EV/risk 0.165 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €130.20–€131.55 (mid €130.88)
- Spot actuel : €138.60 (+5.9% au-dessus de la zone — repli à attendre)
- Stop : €125.82 (stop swing_plan-based (-9.22%))
- Targets : T1 €134.25 · R/R 0.67 | T2 €137.62 · R/R 1.33 | T3 €140.99 · R/R 2.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €125.82


## Edge, scénarios & sizing

- EV/risk : -0.029 | EV/share : €-0.146 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 27 % | T3 12 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 22.6 | bear 48.7 | side 28.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.533% → cible +1.152% / stop −8.0%, p_fill 40%, n_eff≈15.7) : P(cible|rempli) **40%** · **EV/risk +0.005** (×p_fill ; si rempli +0.11% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→66% · +1.0%→52% · +2.0%→28% · +3.0%→12% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.11% (p90 5.26%) · excursion haute méd. +1.05% / basse méd. −1.43%
- Profil de vol intra : ouverture 1.824% vs midi 0.562% vs clôture 0.777% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 92% · range 8% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 18%)_
- **Régime intraday** : **chop** _(efficiency 0.105 ; neutre — autocorr -0.029)_ ; drift intra méd. -0.638% ; recovery-V 15%
- **σ réalisé intraday** 2.286% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 72% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 140.5762 (VA 139.9237–141.6637 ; dernier close 140.05)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 23% · rebond 57% · **stop −1.95%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.79 (high win-rate)
- Gaps overnight (n=149) : méd. 0.2% · baisse 35% (gap-down >1% 9% · >2% 2%)
- Excursion ouverture 5min (n=150) : bas méd −0.51% (p90 −2.12%) · haut méd +0.3% · range méd 1.11%
- Excursion ouverture 15min (n=150) : bas méd −0.59% (p90 −2.22%) · haut méd +0.39% · range méd 1.39%
- Excursion ouverture 30min (n=150) : bas méd −0.6% (p90 −2.36%) · haut méd +0.47% · range méd 1.44%
- Excursion ouverture 60min (n=150) : bas méd −0.86% (p90 −2.59%) · haut méd +0.59% · range méd 1.62%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 140.05 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 71% (106/149) · gap 21% · délai 0.5min · rebond 47% (52/106) (MFE +0.87%)
   - −1.0% : fill 30min 40% · séance 63% (89/149) · gap 9% · délai 9.5min · rebond 50% (43/89) (MFE +0.98%)
   - −1.5% : fill 30min 24% · séance 51% (67/149) · gap 2% · délai 32.4min · rebond 52% (33/67) (MFE +1.08%)
   - −2.0% : fill 30min 15% · séance 34% (49/149) · gap 2% · délai 56.4min · rebond 49% (26/49) (MFE +0.99%)
   - −3.0% : fill 30min 4% · séance 23% (31/149) · gap 1% · délai 115.7min · rebond 57% (18/31) (MFE +1.55%)
   - −4.0% : fill 30min 1% · séance 8% (11/149) · gap 1% · délai 369.3min · rebond 16% (4/11) (MFE +0.77%)
   - −5.0% : fill 30min 1% · séance 2% (4/149) · gap 0% · délai 184.5min · rebond 89% (3/4) (MFE +1.52%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.14% (p90 −1.53%) → stop au-delà de −0.79% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.14% (p90 −1.79%) → stop au-delà de −0.6% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.16% (p90 −0.92%) → stop au-delà de −0.55% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=319 jambes) : jambe baissière méd −1.08% (p90 −2.46%) · ~6.3 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 80% (36/44) · rebond 44% (15/36)
      · −2.0% : fill 45% (25/44) · rebond 43% (13/25)
      · −3.0% : fill 31% (16/44) · rebond 47% (9/16)
      · −4.0% : fill 15% (7/44) · rebond 28% (3/7)
      · −5.0% : fill 8% (4/44) · rebond 89% (3/4)
   - **flat** (36 séances) :
      · −1.0% : fill 70% (24/36) · rebond 49% (13/24)
      · −2.0% : fill 40% (12/36) · rebond 51% (6/12)
      · −3.0% : fill 30% (8/36) · rebond 46% (3/8)
      · −4.0% : fill 10% (2/36) · rebond 0% (0/2)
      · −5.0% : fill 0% (0/36) · rebond 0% (0/0)
   - **gap-up** (69 séances) :
      · −1.0% : fill 51% (29/69) · rebond 55% (15/29)
      · −2.0% : fill 24% (12/69) · rebond 53% (7/12)
      · −3.0% : fill 15% (7/69) · rebond 82% (6/7)
      · −4.0% : fill 3% (2/69) · rebond 15% (1/2)
      · −5.0% : fill 0% (0/69) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 43% en base · 64% si les 15 1res min sont vertes (80 cas) · 19% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=150) : COUDE à **29min** → P(séance verte=clôture>ouverture) 71% si début vert vs 19% si rouge (base 43% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 306min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **71%** · continue >prix actuel 47% ; creux résiduel méd -1.05% (q20 -2.01%) → **SL/trailing à −2.01%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +0.97% / q75 +1.64% → **scale +0.97% / runner +1.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **19%** (continue à baisser 55%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.26%** (au-delà de la MAE q10 -3.26%), cible rebond +1.16% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-2.05% .. +2.11%] · haut q95 +2.51% · bas q05 -2.7%
   - 60min (n=150) : retour [-2.87% .. +2.08%] · haut q95 +2.67% · bas q05 -3.25%
   - 2h (n=150) : retour [-3.62% .. +2.27%] · haut q95 +2.93% · bas q05 -3.78%
   - 4h (n=150) : retour [-3.41% .. +2.34%] · haut q95 +2.94% · bas q05 -4.0%
   - 6h (n=150) : retour [-3.82% .. +3.11%] · haut q95 +3.47% · bas q05 -4.18%
   - session (n=150) : retour [-3.61% .. +2.82%] · haut q95 +3.84% · bas q05 -4.76%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — NEX = **plat / peu volatil** (vol intra méd 1.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.4  _(momentum haussier)_
- **ADX** : 26.4  _(tendance etablie)_
- **MACD** : hist 1.613  _(pas de croisement recent)_
- **BB** : %B 0.8 · largeur 11.8%
- **ATR** : 5.06 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.009  _(neutre)_
- **Vol ratio** : 0.28  _(volume atone)_
- **Choppiness** : 50.0  _(transition)_
- **MA** : MA20 133.83 · MA50 141.97 · MA200 132.08  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 -2.4% · MA200 +4.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92219 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
