# SRT3

**Generated** : 2026-07-09T00:03:21.975744+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €222.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot €222.30 (+0.8% vs entrée) · entrée €220.47 · stop €217.24 · T1 €226.94 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % _(réel 5 s)_ · EV/risk 0.018 _(réel 5 s)_ (GBM 0.041) · ¼-Kelly 0.006 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

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

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €219.18–€221.76 (mid €220.47)
- Spot actuel : €222.30 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : €217.24 (stop swing_plan-based (-2.28%))
- Targets : T1 €226.94 · R/R 2.0 | T2 €233.41 · R/R 4.01 | T3 €239.88 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €217.24


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : €0.132 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 19 % | T3 9 %
- Kelly (position) : f* 0.024 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 40.4 | bear 11.8 | side 47.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.371% → cible +1.312% / stop −3.0%, p_fill 84%, n_eff≈33.9) : P(cible|rempli) **53%** · **EV/risk -0.009** (×p_fill ; si rempli -0.03% du capital)
  - **swing** (entrée dip −0.825% → cible +2.934% / stop −1.467%, p_fill 79%, n_eff≈31.4) : P(cible|rempli) **36%** · **EV/risk +0.018** (×p_fill ; si rempli +0.03% du capital)
  - **deep** (entrée dip −1.272% → cible +4.149% / stop −2.075%, p_fill 76%, n_eff≈31.9) : P(cible|rempli) **39%** · **EV/risk +0.081** (×p_fill ; si rempli +0.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→72% · +2.0%→45% · +3.0%→24% · +5.0%→9% · +8.0%→0%
- Range intraday médian 3.61% (p90 6.59%) · excursion haute méd. +1.89% / basse méd. −1.84%
- Profil de vol intra : ouverture 2.016% vs midi 0.889% vs clôture 0.994% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 8% · trend ↑1%/↓0% ; spike-down 52% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; momentum — autocorr 0.031)_ ; drift intra méd. 0.096% ; recovery-V 27%
- **σ réalisé intraday** 2.354% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 62% / whipsaw 31%
- POC intraday (dernière séance, temps-au-prix) : 231.2556 (VA 229.8719–232.3319 ; dernier close 228.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 56% · rebond 66% · **stop −2.56%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.26% (p90 −1.74%) · haut méd +0.6% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.49% (p90 −1.87%) · haut méd +0.68% · range méd 1.6%
- Excursion ouverture 30min (n=160) : bas méd −0.53% (p90 −2.01%) · haut méd +0.93% · range méd 1.74%
- Excursion ouverture 60min (n=160) : bas méd −0.65% (p90 −2.32%) · haut méd +0.96% · range méd 1.91%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 228.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 76% (122/159) · gap 29% · délai 0.2min · rebond 53% (57/122) (MFE +1.11%)
   - −1.0% : fill 30min 43% · séance 63% (103/159) · gap 17% · délai 0.7min · rebond 58% (58/103) (MFE +1.2%)
   - −1.5% : fill 30min 31% · séance 56% (90/159) · gap 10% · délai 14.9min · rebond 66% (54/90) (MFE +1.56%)
   - −2.0% : fill 30min 21% · séance 42% (69/159) · gap 6% · délai 30.7min · rebond 58% (43/69) (MFE +1.33%)
   - −3.0% : fill 30min 6% · séance 22% (40/159) · gap 2% · délai 184.1min · rebond 54% (24/40) (MFE +1.51%)
   - −4.0% : fill 30min 4% · séance 12% (20/159) · gap 1% · délai 208.7min · rebond 67% (15/20) (MFE +1.31%)
   - −5.0% : fill 30min 1% · séance 7% (10/159) · gap 1% · délai 99.8min · rebond 74% (8/10) (MFE +2.47%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.15% (p90 −1.8%) → stop au-delà de −0.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.13% (p90 −1.88%) → stop au-delà de −0.89% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.13% (p90 −2.09%) → stop au-delà de −1.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=411 jambes) : jambe baissière méd −1.05% (p90 −2.43%) · ~7.0 jambes/séance
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
      · −1.0% : fill 40% (20/47) · rebond 59% (10/20)
      · −2.0% : fill 18% (12/47) · rebond 72% (8/12)
      · −3.0% : fill 6% (5/47) · rebond 52% (3/5)
      · −4.0% : fill 2% (1/47) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/47) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 61% si les 15 1res min sont vertes (90 cas) · 42% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **2:17** → P(séance verte=clôture>ouverture) 77% si début vert vs 29% si rouge (base 54% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 292min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **77%** · continue >prix actuel 53% ; creux résiduel méd -0.98% (q20 -2.15%) → **SL/trailing à −2.15%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.18% / q75 +1.94% → **scale +1.18% / runner +1.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **29%** (continue à baisser 51%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.05%** (au-delà de la MAE q10 -3.05%), cible rebond +1.28% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.13% .. +2.11%] · haut q95 +2.63% · bas q05 -2.76%
   - 60min (n=160) : retour [-2.48% .. +2.31%] · haut q95 +2.74% · bas q05 -3.13%
   - 2h (n=160) : retour [-2.25% .. +2.59%] · haut q95 +3.08% · bas q05 -3.19%
   - 4h (n=160) : retour [-2.65% .. +2.48%] · haut q95 +3.33% · bas q05 -3.54%
   - 6h (n=160) : retour [-2.69% .. +3.42%] · haut q95 +3.9% · bas q05 -3.85%
   - session (n=160) : retour [-3.57% .. +4.15%] · haut q95 +5.59% · bas q05 -4.44%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — SRT3 = **plat / peu volatil** (vol intra méd 2.22%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 54.6  _(neutre)_
- **ADX** : 11.2  _(pas de tendance nette)_
- **MACD** : hist 0.372  _(pas de croisement recent)_
- **BB** : %B 0.39 · largeur 11.9%
- **ATR** : 8.27 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.122  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 59.6  _(transition)_
- **MA** : MA20 225.2 · MA50 226.77 · MA200 230.03  _(prix < MA20)_
- **Dist MA** : MA20 -1.3% · MA50 -2.0% · MA200 -3.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90653 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
