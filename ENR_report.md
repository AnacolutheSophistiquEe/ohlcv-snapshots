# ENR

**Generated** : 2026-07-07T21:40:14.538689+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €155.30  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot €155.30 (+1.3% vs entrée) · entrée €153.34 · stop €149.47 · T1 €161.08 · R/R 2.0  
> ↳ P(T1 av. stop) 26 % _(réel 5 s)_ · EV/risk -0.198 _(réel 5 s)_ (GBM 0.128) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.030 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €151.79–€154.89 (mid €153.34)
- Spot actuel : €155.30 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : €149.47 (stop swing_plan-based (-3.75%))
- Targets : T1 €161.08 · R/R 2.0 | T2 €168.81 · R/R 4.0 | T3 €176.55 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €149.47


## Edge, scénarios & sizing

- EV/risk : 0.128 | EV/share : €0.494 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 11 % | T3 3 %
- Kelly (position) : f* 0.036 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 48.4 | bear 41.9 | side 9.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 155.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.576% → cible +2.256% / stop −8.0%, p_fill 81%, n_eff≈33.5) : P(cible|rempli) **24%** · **EV/risk -0.051** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −1.259% → cible +5.045% / stop −2.522%, p_fill 75%, n_eff≈30.7) : P(cible|rempli) **26%** · **EV/risk -0.198** (×p_fill ; si rempli -0.67% du capital)
  - **deep** (entrée dip −1.953% → cible +7.134% / stop −3.567%, p_fill 81%, n_eff≈32.7) : P(cible|rempli) **25%** · **EV/risk -0.229** (×p_fill ; si rempli -1.00% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→64% · +2.0%→49% · +3.0%→26% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.34% (p90 6.09%) · excursion haute méd. +1.66% / basse méd. −1.74%
- Profil de vol intra : ouverture 2.163% vs midi 0.983% vs clôture 1.195% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; neutre — autocorr -0.005)_ ; drift intra méd. -0.157% ; recovery-V 26%
- **σ réalisé intraday** 2.603% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 69% / bas 61% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 166.08 (VA 165.12–166.4 ; dernier close 170.06)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 75% · **stop −1.45%** sous le fill (sous le bruit) · cible +1.51% · R/R 1.04 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 39% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.65% (p90 −1.83%) · haut méd +0.45% · range méd 1.24%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.22%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.54%) · haut méd +0.61% · range méd 1.85%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.6%) · haut méd +0.73% · range méd 2.03%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 170.06 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 72% (113/159) · gap 27% · délai 0.4min · rebond 53% (58/113) (MFE +1.19%)
   - −1.0% : fill 30min 50% · séance 66% (101/159) · gap 21% · délai 1.3min · rebond 57% (59/101) (MFE +1.34%)
   - −1.5% : fill 30min 40% · séance 61% (88/159) · gap 18% · délai 12.0min · rebond 64% (56/88) (MFE +1.59%)
   - −2.0% : fill 30min 25% · séance 44% (64/159) · gap 12% · délai 11.3min · rebond 63% (39/64) (MFE +1.41%)
   - −3.0% : fill 30min 16% · séance 33% (47/159) · gap 4% · délai 125.9min · rebond 70% (35/47) (MFE +1.61%)
   - −4.0% : fill 30min 8% · séance 24% (36/159) · gap 2% · délai 302.8min · rebond 65% (25/36) (MFE +1.67%)
   - −5.0% : fill 30min 2% · séance 16% (20/159) · gap 1% · délai 391.7min · rebond 75% (14/20) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.9%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.21%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.52%) → stop au-delà de −0.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=487 jambes) : jambe baissière méd −1.04% (p90 −2.55%) · ~7.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 96% (44/45) · rebond 58% (25/44)
      · −2.0% : fill 71% (32/45) · rebond 68% (22/32)
      · −3.0% : fill 60% (27/45) · rebond 67% (20/27)
      · −4.0% : fill 49% (22/45) · rebond 62% (16/22)
      · −5.0% : fill 34% (14/45) · rebond 74% (10/14)
   - **flat** (28 séances) :
      · −1.0% : fill 71% (20/28) · rebond 69% (14/20)
      · −2.0% : fill 35% (9/28) · rebond 56% (4/9)
      · −3.0% : fill 18% (5/28) · rebond 80% (3/5)
      · −4.0% : fill 15% (4/28) · rebond 76% (2/4)
      · −5.0% : fill 9% (2/28) · rebond 74% (1/2)
   - **gap-up** (86 séances) :
      · −1.0% : fill 48% (37/86) · rebond 52% (20/37)
      · −2.0% : fill 32% (23/86) · rebond 60% (13/23)
      · −3.0% : fill 21% (15/86) · rebond 73% (12/15)
      · −4.0% : fill 13% (10/86) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 86% si les 15 1res min sont vertes (77 cas) · 24% si rouges (83 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 24% si rouge (base 51% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **86%** · continue >prix actuel 73% ; creux résiduel méd -1.09% (q20 -2.24%) → **SL/trailing à −2.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.3% → **scale +2.05% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **24%** (continue à baisser 62%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.13%** (au-delà de la MAE q10 -5.13%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.28% .. +2.03%] · haut q95 +2.7% · bas q05 -2.98%
   - 60min (n=160) : retour [-2.35% .. +2.15%] · haut q95 +2.76% · bas q05 -3.26%
   - 2h (n=160) : retour [-2.9% .. +2.46%] · haut q95 +3.25% · bas q05 -3.69%
   - 4h (n=160) : retour [-2.91% .. +2.66%] · haut q95 +4.12% · bas q05 -3.84%
   - 6h (n=160) : retour [-3.17% .. +3.77%] · haut q95 +4.74% · bas q05 -4.43%
   - session (n=160) : retour [-4.89% .. +4.4%] · haut q95 +5.61% · bas q05 -5.97%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 45.2  _(neutre)_
- **ADX** : 13.7  _(pas de tendance nette)_
- **MACD** : hist 0.537  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 20.5%
- **ATR** : 8.04 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.032  _(neutre)_
- **Vol ratio** : 1.16  _(volume normal)_
- **Choppiness** : 61.1  _(transition)_
- **MA** : MA20 160.32 · MA50 166.82 · MA200 140.27  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 -6.9% · MA200 +10.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (94062 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
