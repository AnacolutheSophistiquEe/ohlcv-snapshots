# RHM

**Generated** : 2026-07-31T21:36:05.769472+00:00  
**Santé technique** : 6/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1140.00  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot €1140.00 (+0.5% vs entrée) · entrée €1134.71 · stop €1116.88 · T1 €1170.37 · R/R 2.0  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.368 _(réel 5 s)_ (GBM 0.101) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €1129.41–€1140.00 (mid €1134.71)
- Spot actuel : €1140.00 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €1116.88 (stop swing_plan-based (-2.03%))
- Targets : T1 €1170.37 · R/R 2.0 | T2 €1206.03 · R/R 4.0 | T3 €1241.70 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1116.88


## Edge, scénarios & sizing

- EV/risk : 0.101 | EV/share : €1.791 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 70.4 | bear 5.0 | side 24.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.296% → cible +1.406% / stop −2.0%, p_fill 86%, n_eff≈37.0) : P(cible|rempli) **38%** · **EV/risk -0.092** (×p_fill ; si rempli -0.21% du capital)
  - **swing** (entrée dip −0.466% → cible +3.143% / stop −1.571%, p_fill 91%, n_eff≈38.0) : P(cible|rempli) **50%** · **EV/risk +0.368** (×p_fill ; si rempli +0.64% du capital)
  - **deep** (entrée dip −0.642% → cible +4.445% / stop −2.222%, p_fill 98%, n_eff≈38.8) : P(cible|rempli) **37%** · **EV/risk +0.068** (×p_fill ; si rempli +0.15% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→65% · +2.0%→49% · +3.0%→28% · +5.0%→2% · +8.0%→1%
- Range intraday médian 3.96% (p90 6.86%) · excursion haute méd. +1.98% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.464% vs midi 0.889% vs clôture 1.088% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.096 ; neutre — autocorr -0.019)_ ; drift intra méd. 0.2% ; recovery-V 49%
- **σ réalisé intraday** 2.834% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 79% / bas 61% / whipsaw 40%
- POC intraday (dernière séance, temps-au-prix) : 1062.83 (VA 1059.61–1152.99 ; dernier close 1153.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 60% · **stop −3.16%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 40% (gap-down >1% 11% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.69%) · haut méd +0.62% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −1.98%) · haut méd +0.71% · range méd 1.87%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.32%) · haut méd +0.88% · range méd 2.03%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.62%) · haut méd +1.0% · range méd 2.2%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1153.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (120/159) · gap 27% · délai 0.3min · rebond 60% (64/120) (MFE +1.36%)
   - −1.0% : fill 30min 45% · séance 66% (108/159) · gap 11% · délai 5.3min · rebond 63% (64/108) (MFE +1.41%)
   - −1.5% : fill 30min 29% · séance 53% (81/159) · gap 6% · délai 20.8min · rebond 53% (43/81) (MFE +1.19%)
   - −2.0% : fill 30min 20% · séance 44% (70/159) · gap 5% · délai 32.1min · rebond 63% (43/70) (MFE +1.35%)
   - −3.0% : fill 30min 9% · séance 28% (45/159) · gap 2% · délai 119.5min · rebond 60% (27/45) (MFE +1.31%)
   - −4.0% : fill 30min 4% · séance 20% (27/159) · gap 1% · délai 152.8min · rebond 60% (15/27) (MFE +1.45%)
   - −5.0% : fill 30min 1% · séance 10% (15/159) · gap 1% · délai 201.2min · rebond 48% (7/15) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.76% (p90 −1.76%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −1.87%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.97%) → stop au-delà de −1.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=473 jambes) : jambe baissière méd −1.07% (p90 −2.52%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 94% (49/51) · rebond 63% (28/49)
      · −2.0% : fill 77% (38/51) · rebond 64% (25/38)
      · −3.0% : fill 49% (26/51) · rebond 59% (16/26)
      · −4.0% : fill 36% (15/51) · rebond 70% (10/15)
      · −5.0% : fill 16% (8/51) · rebond 76% (6/8)
   - **flat** (50 séances) :
      · −1.0% : fill 67% (36/50) · rebond 69% (24/36)
      · −2.0% : fill 28% (17/50) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/50) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/50) · rebond 22% (1/6)
   - **gap-up** (58 séances) :
      · −1.0% : fill 42% (23/58) · rebond 55% (12/23)
      · −2.0% : fill 28% (15/58) · rebond 55% (8/15)
      · −3.0% : fill 18% (9/58) · rebond 66% (6/9)
      · −4.0% : fill 10% (4/58) · rebond 61% (3/4)
      · −5.0% : fill 4% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 56% en base · 72% si les 15 1res min sont vertes (83 cas) · 40% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 80% si début vert vs 31% si rouge (base 56% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **80%** · continue >prix actuel 53% ; creux résiduel méd -0.94% (q20 -1.95%) → **SL/trailing à −1.95%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.43% / q75 +2.16% → **scale +1.43% / runner +2.16%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **31%** (continue à baisser 52%) → **RÉDUIRE ~69%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.55%** (au-delà de la MAE q10 -4.55%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +2.98%] · haut q95 +3.7% · bas q05 -3.08%
   - 60min (n=160) : retour [-3.12% .. +2.94%] · haut q95 +3.85% · bas q05 -3.78%
   - 2h (n=160) : retour [-3.48% .. +3.01%] · haut q95 +4.03% · bas q05 -4.45%
   - 4h (n=160) : retour [-3.38% .. +3.21%] · haut q95 +4.57% · bas q05 -5.01%
   - 6h (n=160) : retour [-4.44% .. +3.66%] · haut q95 +4.57% · bas q05 -5.66%
   - session (n=160) : retour [-6.16% .. +4.45%] · haut q95 +4.84% · bas q05 -6.45%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.3%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : stretched_up
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

- **RSI** : 86.5  _(surachat)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist 23.711  _(pas de croisement recent)_
- **BB** : %B 0.89 · largeur 24.6%
- **ATR** : 43.44 (2.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.007  _(neutre)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 33.5  _(marche directionnel)_
- **MA** : MA20 1040.37 · MA50 1107.88 · MA200 1458.88  _(prix > MA20)_
- **Dist MA** : MA20 +9.6% · MA50 +2.9% · MA200 -21.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90710 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
