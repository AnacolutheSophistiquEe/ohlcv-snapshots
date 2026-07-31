# PRY

**Generated** : 2026-07-31T00:10:33.739314+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €118.95  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €118.95 (+0.6% vs entrée) · entrée €118.20 · stop €115.70 · T1 €123.20 · R/R 2.0  
> ↳ P(T1 av. stop) 8 % _(réel 5 s)_ · EV/risk -0.323 _(réel 5 s)_ (GBM -0.01) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.12% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -51 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €117.81–€118.59 (mid €118.20)
- Spot actuel : €118.95 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €115.70 (stop swing_plan-based (-3.2%))
- Targets : T1 €123.20 · R/R 2.0 | T2 €123.62 · R/R 2.17 | T3 €124.05 · R/R 2.34
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €115.70


## Edge, scénarios & sizing

- EV/risk : -0.01 | EV/share : €-0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 9 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 33.5 | bear 49.6 | side 16.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.628% → cible +4.23% / stop −2.115%, p_fill 79%, n_eff≈30.9) : P(cible|rempli) **8%** · **EV/risk -0.323** (×p_fill ; si rempli -0.87% du capital)
  - **swing** (entrée dip −1.382% → cible +3.686% / stop −1.843%, p_fill 69%, n_eff≈26.5) : P(cible|rempli) **22%** · **EV/risk -0.269** (×p_fill ; si rempli -0.72% du capital)
  - **deep** (entrée dip −2.139% → cible +5.213% / stop −2.606%, p_fill 81%, n_eff≈30.0) : P(cible|rempli) **20%** · **EV/risk -0.350** (×p_fill ; si rempli -1.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→64% · +2.0%→39% · +3.0%→28% · +5.0%→9% · +8.0%→4%
- Range intraday médian 3.92% (p90 6.33%) · excursion haute méd. +1.45% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.291% vs midi 0.825% vs clôture 1.142% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; neutre — autocorr 0.009)_ ; drift intra méd. -0.762% ; recovery-V 15%
- **σ réalisé intraday** 2.692% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 68% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 116.453 (VA 115.577–117.329 ; dernier close 114.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=142) : méd. 0.13% · baisse 44% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=143) : bas méd −0.71% (p90 −2.03%) · haut méd +0.58% · range méd 1.38%
- Excursion ouverture 15min (n=143) : bas méd −0.91% (p90 −2.26%) · haut méd +0.73% · range méd 1.73%
- Excursion ouverture 30min (n=143) : bas méd −0.93% (p90 −2.91%) · haut méd +0.86% · range méd 1.87%
- Excursion ouverture 60min (n=143) : bas méd −1.17% (p90 −3.04%) · haut méd +0.9% · range méd 2.12%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 114.5 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 73% (104/142) · gap 30% · délai 0.2min · rebond 60% (65/104) (MFE +1.23%)
   - −1.0% : fill 30min 51% · séance 64% (88/142) · gap 22% · délai 0.3min · rebond 56% (52/88) (MFE +1.47%)
   - −1.5% : fill 30min 36% · séance 55% (76/142) · gap 18% · délai 0.4min · rebond 50% (41/76) (MFE +0.95%)
   - −2.0% : fill 30min 25% · séance 47% (62/142) · gap 12% · délai 13.0min · rebond 56% (38/62) (MFE +1.16%)
   - −3.0% : fill 30min 15% · séance 36% (45/142) · gap 4% · délai 76.7min · rebond 62% (30/45) (MFE +1.58%)
   - −4.0% : fill 30min 4% · séance 23% (25/142) · gap 2% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 2% · séance 15% (17/142) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.28% (p90 −1.75%) → stop au-delà de −1.49% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.2% (p90 −1.6%) → stop au-delà de −1.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.54%) → stop au-delà de −1.01% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=436 jambes) : jambe baissière méd −1.11% (p90 −2.49%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 90% (47/52) · rebond 46% (26/47)
      · −2.0% : fill 73% (38/52) · rebond 64% (26/38)
      · −3.0% : fill 60% (29/52) · rebond 71% (22/29)
      · −4.0% : fill 38% (16/52) · rebond 65% (11/16)
      · −5.0% : fill 29% (12/52) · rebond 73% (9/12)
   - **flat** (26 séances) :
      · −1.0% : fill 65% (14/26) · rebond 66% (9/14)
      · −2.0% : fill 38% (7/26) · rebond 82% (5/7)
      · −3.0% : fill 25% (5/26) · rebond 40% (2/5)
      · −4.0% : fill 12% (3/26) · rebond 59% (2/3)
      · −5.0% : fill 6% (2/26) · rebond 25% (1/2)
   - **gap-up** (64 séances) :
      · −1.0% : fill 44% (27/64) · rebond 66% (17/27)
      · −2.0% : fill 28% (17/64) · rebond 26% (7/17)
      · −3.0% : fill 21% (11/64) · rebond 48% (6/11)
      · −4.0% : fill 15% (6/64) · rebond 86% (5/6)
      · −5.0% : fill 7% (3/64) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 47% en base · 72% si les 15 1res min sont vertes (67 cas) · 26% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=143) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 83% si début vert vs 20% si rouge (base 47% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -1.3% (q20 -2.09%) → **SL/trailing à −2.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +2.48% → **scale +1.33% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **20%** (continue à baisser 68%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.11%** (au-delà de la MAE q10 -4.11%), cible rebond +1.2% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-2.83% .. +2.86%] · haut q95 +3.84% · bas q05 -3.33%
   - 60min (n=143) : retour [-2.88% .. +2.26%] · haut q95 +4.06% · bas q05 -3.46%
   - 2h (n=143) : retour [-3.57% .. +3.13%] · haut q95 +4.11% · bas q05 -3.67%
   - 4h (n=143) : retour [-3.46% .. +3.48%] · haut q95 +4.53% · bas q05 -4.43%
   - 6h (n=143) : retour [-3.7% .. +3.74%] · haut q95 +4.86% · bas q05 -4.6%
   - session (n=143) : retour [-4.87% .. +4.78%] · haut q95 +5.83% · bas q05 -6.12%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.9% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 32.5  _(momentum baissier)_
- **ADX** : 34.8  _(tendance etablie)_
- **MACD** : hist -1.24  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 25.4%
- **ATR** : 5.98 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.097  _(distribution)_
- **Vol ratio** : 1.87  _(volume au-dessus de la moyenne)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 129.99 · MA50 140.45 · MA200 110.24  _(prix < MA20)_
- **Dist MA** : MA20 -8.5% · MA50 -15.3% · MA200 +7.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91050 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
