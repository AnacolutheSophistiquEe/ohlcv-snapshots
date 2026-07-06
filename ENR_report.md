# ENR

**Generated** : 2026-07-06T00:05:05.036990+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €168.12  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €168.12 (+0.6% vs entrée) · entrée €167.09 · stop €155.99 · T1 €189.28 · R/R 2.0  
> ↳ P(T1 av. stop) 3 % _(réel 5 s)_ · EV/risk -0.198 _(réel 5 s)_ (GBM 0.064) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €166.06–€168.12 (mid €167.09)
- Spot actuel : €168.12 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €155.99 (stop swing_plan-based (-7.21%))
- Targets : T1 €189.28 · R/R 2.0 | T2 €189.76 · R/R 2.04 | T3 €190.25 · R/R 2.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €155.99


## Edge, scénarios & sizing

- EV/risk : 0.064 | EV/share : €0.711 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 6 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 52.5 | bear 24.9 | side 22.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 504.0 (= 3 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.361% → cible +2.066% / stop −3.0%, p_fill 86%, n_eff≈35.0) : P(cible|rempli) **31%** · **EV/risk -0.179** (×p_fill ; si rempli -0.62% du capital)
  - **swing** (entrée dip −0.61% → cible +13.28% / stop −6.64%, p_fill 87%, n_eff≈33.8) : P(cible|rempli) **3%** · **EV/risk -0.198** (×p_fill ; si rempli -1.52% du capital)
  - **deep** (entrée dip −0.882% → cible +6.533% / stop −3.267%, p_fill 86%, n_eff≈34.4) : P(cible|rempli) **32%** · **EV/risk -0.091** (×p_fill ; si rempli -0.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→65% · +2.0%→50% · +3.0%→28% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.36% (p90 6.09%) · excursion haute méd. +1.9% / basse méd. −1.73%
- Profil de vol intra : ouverture 2.146% vs midi 0.987% vs clôture 1.202% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.016)_ ; drift intra méd. -0.179% ; recovery-V 21%
- **σ réalisé intraday** 2.579% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 64% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 167.604 (VA 166.988–168.132 ; dernier close 169.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 16% · rebond 75% · **stop −1.45%** sous le fill (sous le bruit) · cible +1.51% · R/R 1.04 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 39% (gap-down >1% 21% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −0.64% (p90 −1.73%) · haut méd +0.45% · range méd 1.23%
- Excursion ouverture 15min (n=160) : bas méd −0.71% (p90 −2.21%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.9% (p90 −2.38%) · haut méd +0.61% · range méd 1.83%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.57%) · haut méd +0.76% · range méd 2.02%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 169.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 57% · séance 72% (113/159) · gap 28% · délai 0.4min · rebond 52% (57/113) (MFE +1.11%)
   - −1.0% : fill 30min 49% · séance 66% (101/159) · gap 21% · délai 1.4min · rebond 56% (59/101) (MFE +1.31%)
   - −1.5% : fill 30min 38% · séance 60% (88/159) · gap 18% · délai 12.9min · rebond 63% (56/88) (MFE +1.54%)
   - −2.0% : fill 30min 24% · séance 44% (64/159) · gap 12% · délai 16.9min · rebond 62% (39/64) (MFE +1.38%)
   - −3.0% : fill 30min 16% · séance 33% (48/159) · gap 4% · délai 127.7min · rebond 70% (36/48) (MFE +1.63%)
   - −4.0% : fill 30min 8% · séance 25% (36/159) · gap 2% · délai 302.8min · rebond 65% (25/36) (MFE +1.67%)
   - −5.0% : fill 30min 2% · séance 16% (20/159) · gap 1% · délai 391.7min · rebond 75% (14/20) (MFE +1.51%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −1.9%) → stop au-delà de −1.03% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −2.21%) → stop au-delà de −1.51% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.52%) → stop au-delà de −0.85% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=490 jambes) : jambe baissière méd −1.06% (p90 −2.52%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (45 séances) :
      · −1.0% : fill 96% (44/45) · rebond 58% (25/44)
      · −2.0% : fill 71% (32/45) · rebond 68% (22/32)
      · −3.0% : fill 60% (27/45) · rebond 67% (20/27)
      · −4.0% : fill 49% (22/45) · rebond 62% (16/22)
      · −5.0% : fill 34% (14/45) · rebond 74% (10/14)
   - **flat** (27 séances) :
      · −1.0% : fill 67% (19/27) · rebond 63% (13/19)
      · −2.0% : fill 27% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 20% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 17% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 11% (2/27) · rebond 74% (1/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 48% (38/87) · rebond 52% (21/38)
      · −2.0% : fill 32% (24/87) · rebond 60% (14/24)
      · −3.0% : fill 21% (16/87) · rebond 74% (13/16)
      · −4.0% : fill 13% (10/87) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/87) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 86% si les 15 1res min sont vertes (78 cas) · 22% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **15min** → P(séance verte=clôture>ouverture) 86% si début vert vs 22% si rouge (base 50% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 227min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **86%** · continue >prix actuel 73% ; creux résiduel méd -1.09% (q20 -2.24%) → **SL/trailing à −2.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.05% / q75 +3.3% → **scale +2.05% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **22%** (continue à baisser 64%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.17%** (au-delà de la MAE q10 -5.17%), cible rebond +1.18% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.04%] · haut q95 +2.72% · bas q05 -2.71%
   - 60min (n=160) : retour [-2.36% .. +2.17%] · haut q95 +2.78% · bas q05 -3.0%
   - 2h (n=160) : retour [-2.94% .. +2.48%] · haut q95 +3.3% · bas q05 -3.72%
   - 4h (n=160) : retour [-2.94% .. +2.66%] · haut q95 +4.13% · bas q05 -3.85%
   - 6h (n=160) : retour [-3.18% .. +3.78%] · haut q95 +4.77% · bas q05 -4.43%
   - session (n=160) : retour [-4.89% .. +4.41%] · haut q95 +5.66% · bas q05 -6.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.42%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 60.7  _(momentum haussier)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist 1.197  _(pas de croisement recent)_
- **BB** : %B 0.77 · largeur 20.7%
- **ATR** : 7.27 (64.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.072  _(distribution)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 57.3  _(transition)_
- **MA** : MA20 159.33 · MA50 167.61 · MA200 139.57  _(prix > MA20)_
- **Dist MA** : MA20 +5.5% · MA50 +0.3% · MA200 +20.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (93187 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
