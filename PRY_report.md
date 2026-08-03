# PRY

**Generated** : 2026-08-03T21:47:14.736494+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €119.45  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €119.45 (+0.7% vs entrée) · entrée €118.58 · stop €116.26 · T1 €123.20 · R/R 1.99  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk -0.351 _(réel 5 s)_ (GBM -0.06) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.95% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €118.19–€118.96 (mid €118.58)
- Spot actuel : €119.45 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : €116.26 (stop swing_plan-based (-6.93%))
- Targets : T1 €123.20 · R/R 1.99 | T2 €123.76 · R/R 2.23 | T3 €124.32 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €116.26


## Edge, scénarios & sizing

- EV/risk : -0.06 | EV/share : €-0.138 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 10 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 28.7 | bear 57.5 | side 13.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.734% → cible +3.9% / stop −1.95%, p_fill 80%, n_eff≈31.1) : P(cible|rempli) **10%** · **EV/risk -0.351** (×p_fill ; si rempli -0.85% du capital)
  - **swing** (entrée dip −1.608% → cible +3.609% / stop −5.409%, p_fill 68%, n_eff≈26.0) : P(cible|rempli) **29%** · **EV/risk -0.325** (×p_fill ; si rempli -2.57% du capital)
  - **deep** (entrée dip −2.487% → cible +5.105% / stop −8.187%, p_fill 76%, n_eff≈27.9) : P(cible|rempli) **35%** · **EV/risk -0.216** (×p_fill ; si rempli -2.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→39% · +3.0%→26% · +5.0%→9% · +8.0%→4%
- Range intraday médian 4.02% (p90 6.42%) · excursion haute méd. +1.37% / basse méd. −1.69%
- Profil de vol intra : ouverture 2.348% vs midi 0.837% vs clôture 1.169% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (145 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 57% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.852% ; recovery-V 20%
- **σ réalisé intraday** 2.874% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 71% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 124.7875 (VA 122.6875–125.1375 ; dernier close 119.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 71% · **stop −2.55%** sous le fill (sous le bruit) · cible +1.37% · R/R 0.54 (high win-rate)
- Gaps overnight (n=144) : méd. 0.29% · baisse 42% (gap-down >1% 21% · >2% 11%)
- Excursion ouverture 5min (n=145) : bas méd −0.82% (p90 −2.26%) · haut méd +0.5% · range méd 1.41%
- Excursion ouverture 15min (n=145) : bas méd −0.92% (p90 −2.84%) · haut méd +0.64% · range méd 1.76%
- Excursion ouverture 30min (n=145) : bas méd −1.01% (p90 −3.02%) · haut méd +0.76% · range méd 1.89%
- Excursion ouverture 60min (n=145) : bas méd −1.23% (p90 −3.23%) · haut méd +0.87% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 119.26 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 61% · séance 72% (105/144) · gap 29% · délai 0.2min · rebond 61% (66/105) (MFE +1.32%)
   - −1.0% : fill 30min 51% · séance 64% (89/144) · gap 21% · délai 0.2min · rebond 57% (53/89) (MFE +1.5%)
   - −1.5% : fill 30min 36% · séance 55% (77/144) · gap 17% · délai 0.4min · rebond 52% (42/77) (MFE +1.09%)
   - −2.0% : fill 30min 26% · séance 47% (63/144) · gap 11% · délai 4.3min · rebond 58% (39/63) (MFE +1.2%)
   - −3.0% : fill 30min 15% · séance 36% (46/144) · gap 4% · délai 71.8min · rebond 63% (31/46) (MFE +1.61%)
   - −4.0% : fill 30min 4% · séance 22% (25/144) · gap 2% · délai 249.0min · rebond 71% (18/25) (MFE +1.37%)
   - −5.0% : fill 30min 2% · séance 14% (17/144) · gap 1% · délai 394.0min · rebond 76% (13/17) (MFE +1.58%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.8%) → stop au-delà de −1.52% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.22% (p90 −1.98%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.02% (p90 −1.54%) → stop au-delà de −1.01% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=451 jambes) : jambe baissière méd −1.08% (p90 −2.61%) · ~7.0 jambes/séance
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
   - **gap-up** (66 séances) :
      · −1.0% : fill 44% (28/66) · rebond 69% (18/28)
      · −2.0% : fill 30% (18/66) · rebond 35% (8/18)
      · −3.0% : fill 23% (12/66) · rebond 57% (7/12)
      · −4.0% : fill 14% (6/66) · rebond 86% (5/6)
      · −5.0% : fill 6% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=145) : 47% en base · 69% si les 15 1res min sont vertes (68 cas) · 29% si rouges (77 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=145) : COUDE à **1:10** → P(séance verte=clôture>ouverture) 83% si début vert vs 22% si rouge (base 47% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 296min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=66) : tient le vert **83%** · continue >prix actuel 62% ; creux résiduel méd -1.3% (q20 -2.09%) → **SL/trailing à −2.09%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.33% / q75 +2.48% → **scale +1.33% / runner +2.48%**, sortie à la clôture
  - **si ROUGE au coude** (n=79) : edge inversé — récupère vert seulement **22%** (continue à baisser 67%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.08%** (au-delà de la MAE q10 -4.08%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=145) : retour [-3.05% .. +2.83%] · haut q95 +3.73% · bas q05 -3.44%
   - 60min (n=145) : retour [-3.17% .. +2.25%] · haut q95 +4.03% · bas q05 -3.53%
   - 2h (n=145) : retour [-3.54% .. +2.98%] · haut q95 +4.1% · bas q05 -4.28%
   - 4h (n=145) : retour [-3.46% .. +3.32%] · haut q95 +4.53% · bas q05 -4.57%
   - 6h (n=145) : retour [-3.7% .. +3.74%] · haut q95 +4.81% · bas q05 -4.78%
   - session (n=145) : retour [-4.81% .. +4.77%] · haut q95 +5.77% · bas q05 -6.24%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.8% des séances seulement sont des jours de hausse propre — PRY = **plat / peu volatil** (vol intra méd 2.41%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 34.8  _(momentum baissier)_
- **ADX** : 35.4  _(tendance etablie)_
- **MACD** : hist -0.911  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 23.5%
- **ATR** : 6.36 (94.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.046  _(neutre)_
- **Vol ratio** : 1.48  _(volume normal)_
- **Choppiness** : 43.8  _(transition)_
- **MA** : MA20 128.69 · MA50 139.86 · MA200 110.41  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -14.6% · MA200 +8.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (91154 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
