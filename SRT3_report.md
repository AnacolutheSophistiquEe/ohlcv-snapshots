# SRT3

**Generated** : 2026-07-07T21:37:23.545524+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €232.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot €232.20 (+3.2% vs entrée) · entrée €224.93 · stop €221.90 · T1 €230.98 · R/R 2.0  
> ↳ P(T1 av. stop) 41 % _(réel 5 s)_ · EV/risk 0.04 _(réel 5 s)_ (GBM -0.018) · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €223.71–€226.14 (mid €224.93)
- Spot actuel : €232.20 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : €221.90 (stop swing_plan-based (-4.44%))
- Targets : T1 €230.98 · R/R 2.0 | T2 €237.04 · R/R 4.0 | T3 €243.10 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €221.90


## Edge, scénarios & sizing

- EV/risk : -0.018 | EV/share : €-0.055 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 17 % | T3 10 %
- Kelly (position) : f* 0.01 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 46.8 | bear 13.7 | side 39.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 232.0 (= 1 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.423% → cible +1.204% / stop −3.0%, p_fill 54%, n_eff≈23.8) : P(cible|rempli) **40%** · **EV/risk -0.026** (×p_fill ; si rempli -0.14% du capital)
  - **swing** (entrée dip −3.136% → cible +2.693% / stop −1.346%, p_fill 27%, n_eff≈12.5) : P(cible|rempli) **41%** · **EV/risk +0.040** (×p_fill ; si rempli +0.20% du capital)
  - **deep** (entrée dip −4.838% → cible +3.808% / stop −1.904%, p_fill 32%, n_eff≈12.3) : P(cible|rempli) **28%** · **EV/risk -0.073** (×p_fill ; si rempli -0.43% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→72% · +2.0%→46% · +3.0%→25% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.63% (p90 6.59%) · excursion haute méd. +1.91% / basse méd. −1.84%
- Profil de vol intra : ouverture 2.035% vs midi 0.89% vs clôture 1.005% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑1%/↓0% ; spike-down 53% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; momentum — autocorr 0.033)_ ; drift intra méd. 0.129% ; recovery-V 27%
- **σ réalisé intraday** 2.355% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 60% / whipsaw 27%
- POC intraday (dernière séance, temps-au-prix) : 228.9925 (VA 228.5825–231.8625 ; dernier close 228.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 57% · rebond 66% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. -0.09% · baisse 52% (gap-down >1% 18% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.27% (p90 −1.76%) · haut méd +0.57% · range méd 1.18%
- Excursion ouverture 15min (n=160) : bas méd −0.51% (p90 −1.87%) · haut méd +0.68% · range méd 1.56%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.01%) · haut méd +0.83% · range méd 1.75%
- Excursion ouverture 60min (n=160) : bas méd −0.66% (p90 −2.35%) · haut méd +0.94% · range méd 1.93%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 228.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 77% (123/159) · gap 29% · délai 0.2min · rebond 53% (57/123) (MFE +1.11%)
   - −1.0% : fill 30min 44% · séance 64% (104/159) · gap 18% · délai 0.7min · rebond 58% (58/104) (MFE +1.19%)
   - −1.5% : fill 30min 32% · séance 57% (91/159) · gap 10% · délai 15.0min · rebond 66% (55/91) (MFE +1.56%)
   - −2.0% : fill 30min 22% · séance 42% (69/159) · gap 6% · délai 30.7min · rebond 58% (43/69) (MFE +1.33%)
   - −3.0% : fill 30min 6% · séance 22% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 12% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 7% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.21% (p90 −1.82%) → stop au-delà de −0.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.88%) → stop au-delà de −0.91% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −2.08%) → stop au-delà de −1.43% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.04% (p90 −2.45%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (76 séances) :
      · −1.0% : fill 81% (62/76) · rebond 68% (39/62)
      · −2.0% : fill 58% (42/76) · rebond 65% (28/42)
      · −3.0% : fill 38% (29/76) · rebond 56% (17/29)
      · −4.0% : fill 20% (16/76) · rebond 71% (12/16)
      · −5.0% : fill 10% (7/76) · rebond 92% (6/7)
   - **flat** (36 séances) :
      · −1.0% : fill 62% (21/36) · rebond 35% (9/21)
      · −2.0% : fill 48% (15/36) · rebond 38% (7/15)
      · −3.0% : fill 18% (6/36) · rebond 49% (4/6)
      · −4.0% : fill 11% (3/36) · rebond 44% (2/3)
      · −5.0% : fill 11% (3/36) · rebond 44% (2/3)
   - **gap-up** (47 séances) :
      · −1.0% : fill 42% (21/47) · rebond 58% (10/21)
      · −2.0% : fill 18% (12/47) · rebond 72% (8/12)
      · −3.0% : fill 6% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 55% en base · 63% si les 15 1res min sont vertes (89 cas) · 42% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 80% si début vert vs 29% si rouge (base 55% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **80%** · continue >prix actuel 55% ; creux résiduel méd -0.89% (q20 -2.18%) → **SL/trailing à −2.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +2.12% → **scale +1.19% / runner +2.12%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **29%** (continue à baisser 51%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.05%** (au-delà de la MAE q10 -3.05%), cible rebond +1.28% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.14% .. +2.11%] · haut q95 +2.63% · bas q05 -2.76%
   - 60min (n=160) : retour [-2.5% .. +2.32%] · haut q95 +2.76% · bas q05 -3.15%
   - 2h (n=160) : retour [-2.25% .. +2.6%] · haut q95 +3.09% · bas q05 -3.19%
   - 4h (n=160) : retour [-2.66% .. +2.52%] · haut q95 +3.34% · bas q05 -3.54%
   - 6h (n=160) : retour [-2.7% .. +3.46%] · haut q95 +3.92% · bas q05 -3.86%
   - session (n=160) : retour [-3.58% .. +4.31%] · haut q95 +5.61% · bas q05 -4.46%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.21%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 53.5  _(neutre)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist 0.915  _(pas de croisement recent)_
- **BB** : %B 0.72 · largeur 12.5%
- **ATR** : 9.03 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.113  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 58.9  _(transition)_
- **MA** : MA20 225.9 · MA50 226.59 · MA200 229.96  _(prix > MA20)_
- **Dist MA** : MA20 +2.8% · MA50 +2.5% · MA200 +1.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93120 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
