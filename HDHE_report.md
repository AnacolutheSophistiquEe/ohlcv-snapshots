# 267260

**Generated** : 2026-07-23T00:14:05.711916+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩795000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩795000.00 (+1.7% vs entrée) · entrée ₩781413.71 · stop ₩718900.62 · T1 ₩832775.15 · R/R 0.82  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk -0.069 _(réel 5 s)_ (GBM -0.172) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩777501.88–₩785325.55 (mid ₩781413.71)
- Spot actuel : ₩795000.00 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : ₩718900.62 (stop swing_plan-based (-6.51%))
- Targets : T1 ₩832775.15 · R/R 0.82 | T2 ₩836344.27 · R/R 0.88 | T3 ₩839913.39 · R/R 0.94
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩718900.62


## Edge, scénarios & sizing

- EV/risk : -0.172 | EV/share : ₩-10720.996 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.6 | bear 70.2 | side 22.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.707% → cible +6.573% / stop −8.0%, p_fill 89%, n_eff≈34.8) : P(cible|rempli) **11%** · **EV/risk -0.069** (×p_fill ; si rempli -0.62% du capital)
  - **swing** (entrée dip −3.758% → cible +5.58% / stop −2.86%, p_fill 79%, n_eff≈30.1) : P(cible|rempli) **21%** · **EV/risk -0.336** (×p_fill ; si rempli -1.22% du capital)
  - **deep** (entrée dip −5.814% → cible +7.891% / stop −3.946%, p_fill 75%, n_eff≈26.9) : P(cible|rempli) **19%** · **EV/risk -0.323** (×p_fill ; si rempli -1.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→68% · +2.0%→45% · +3.0%→29% · +5.0%→10% · +8.0%→5%
- Range intraday médian 6.16% (p90 10.49%) · excursion haute méd. +1.84% / basse méd. −3.53%
- Profil de vol intra : ouverture 3.997% vs midi 1.051% vs clôture 1.142% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (137 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 79% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -1.647% ; recovery-V 20%
- **σ réalisé intraday** 4.842% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 77% / whipsaw 26%
- POC intraday (dernière séance, temps-au-prix) : 777300.0 (VA 759300.0–788100.0 ; dernier close 771000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 84% · **stop −4.2%** sous le fill (sous le bruit) · cible +2.39% · R/R 0.57 (high win-rate)
- Gaps overnight (n=136) : méd. 0.55% · baisse 40% (gap-down >1% 24% · >2% 10%)
- Excursion ouverture 5min (n=137) : bas méd −1.61% (p90 −3.77%) · haut méd +0.92% · range méd 2.68%
- Excursion ouverture 15min (n=137) : bas méd −1.88% (p90 −4.67%) · haut méd +1.06% · range méd 3.33%
- Excursion ouverture 30min (n=137) : bas méd −2.21% (p90 −4.91%) · haut méd +1.08% · range méd 3.69%
- Excursion ouverture 60min (n=137) : bas méd −2.6% (p90 −5.62%) · haut méd +1.26% · range méd 4.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 771000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (97/136) · gap 31% · délai 0.0min · rebond 53% (54/97) (MFE +1.19%)
   - −1.0% : fill 30min 56% · séance 70% (90/136) · gap 24% · délai 0.3min · rebond 53% (52/90) (MFE +1.01%)
   - −1.5% : fill 30min 49% · séance 63% (77/136) · gap 16% · délai 0.5min · rebond 66% (50/77) (MFE +1.28%)
   - −2.0% : fill 30min 44% · séance 60% (70/136) · gap 10% · délai 0.8min · rebond 67% (47/70) (MFE +1.7%)
   - −3.0% : fill 30min 33% · séance 50% (55/136) · gap 6% · délai 5.1min · rebond 77% (38/55) (MFE +1.76%)
   - −4.0% : fill 30min 25% · séance 43% (46/136) · gap 3% · délai 14.8min · rebond 80% (37/46) (MFE +2.33%)
   - −5.0% : fill 30min 15% · séance 36% (36/136) · gap 2% · délai 46.8min · rebond 84% (28/36) (MFE +2.39%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −3.55%) → stop au-delà de −1.96% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.87% (p90 −3.47%) → stop au-delà de −2.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −5.0%) → stop au-delà de −3.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=671 jambes) : jambe baissière méd −1.32% (p90 −3.6%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 98% (46/47) · rebond 46% (24/46)
      · −2.0% : fill 91% (39/47) · rebond 60% (23/39)
      · −3.0% : fill 80% (33/47) · rebond 76% (22/33)
      · −4.0% : fill 71% (29/47) · rebond 83% (24/29)
      · −5.0% : fill 60% (22/47) · rebond 85% (17/22)
   - **flat** (17 séances) :
      · −1.0% : fill 88% (14/17) · rebond 47% (7/14)
      · −2.0% : fill 79% (12/17) · rebond 78% (9/12)
      · −3.0% : fill 78% (11/17) · rebond 83% (8/11)
      · −4.0% : fill 57% (7/17) · rebond 68% (5/7)
      · −5.0% : fill 57% (7/17) · rebond 89% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 49% (30/72) · rebond 64% (21/30)
      · −2.0% : fill 35% (19/72) · rebond 71% (15/19)
      · −3.0% : fill 25% (11/72) · rebond 73% (8/11)
      · −4.0% : fill 23% (10/72) · rebond 82% (8/10)
      · −5.0% : fill 16% (7/72) · rebond 78% (5/7)
- **P(clôture VERTE) selon le drive 15min** (n=137) : 34% en base · 50% si les 15 1res min sont vertes (64 cas) · 24% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=137) : COUDE à **1:20** → P(séance verte=clôture>ouverture) 76% si début vert vs 10% si rouge (base 34% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **76%** · continue >prix actuel 45% ; creux résiduel méd -1.48% (q20 -3.75%) → **SL/trailing à −3.75%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.23% / q75 +2.62% → **scale +1.23% / runner +2.62%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 53%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.21%** (au-delà de la MAE q10 -5.21%), cible rebond +1.64% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=137) : retour [-5.2% .. +2.95%] · haut q95 +4.38% · bas q05 -5.66%
   - 60min (n=137) : retour [-5.59% .. +3.26%] · haut q95 +4.57% · bas q05 -6.03%
   - 2h (n=137) : retour [-6.96% .. +3.66%] · haut q95 +5.45% · bas q05 -7.42%
   - 4h (n=137) : retour [-6.94% .. +4.59%] · haut q95 +5.53% · bas q05 -8.18%
   - 6h (n=137) : retour [-6.93% .. +3.89%] · haut q95 +7.48% · bas q05 -8.84%
   - session (n=137) : retour [-7.09% .. +3.92%] · haut q95 +7.48% · bas q05 -9.13%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 25.7  _(survente)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist -4327.0  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 36.4%
- **ATR** : 72928.57 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.119  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 38.8  _(transition)_
- **MA** : MA20 872150.0 · MA50 1007414.0 · MA200 917207.63  _(prix < MA20)_
- **Dist MA** : MA20 -8.8% · MA50 -21.1% · MA200 -13.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84500 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
