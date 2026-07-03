# RHM

**Generated** : 2026-07-03T21:35:58.883463+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €1093.40  

> 🟡 **WAIT-FOR-DIP** — spot +6.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €1093.40 (+6.6% vs entrée) · entrée €1025.99 · stop €1005.47 · T1 €1056.97 · R/R 1.51  
> ↳ P(T1 av. stop) 30 % · EV/risk 0.017 · ¼-Kelly 0.005 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1019.79–€1032.18 (mid €1025.99)
- Spot actuel : €1093.40 (+6.6% au-dessus de la zone — repli à attendre)
- Stop : €1005.47 (stop swing_plan-based (-15.29%))
- Targets : T1 €1056.97 · R/R 1.51 | T2 €1087.96 · R/R 3.02 | T3 €1118.95 · R/R 4.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1005.47


## Edge, scénarios & sizing

- EV/risk : 0.017 | EV/share : €0.338 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.02 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.5 | bear 27.7 | side 64.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=6, n_eff=3))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→50% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.65%) · excursion haute méd. +2.02% / basse méd. −1.68%
- Profil de vol intra : ouverture 2.505% vs midi 0.881% vs clôture 1.01% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.099 ; neutre — autocorr 0.012)_ ; drift intra méd. -0.174% ; recovery-V 48%
- **σ réalisé intraday** 2.937% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 70% / bas 71% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 1089.275 (VA 1074.955–1119.705 ; dernier close 1117.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 45% · rebond 66% · **stop −3.31%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 40% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −1.72%) · haut méd +0.57% · range méd 1.5%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −1.95%) · haut méd +0.75% · range méd 1.87%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.22%) · haut méd +0.98% · range méd 2.15%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −2.45%) · haut méd +1.01% · range méd 2.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1117.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 74% (118/159) · gap 27% · délai 0.3min · rebond 56% (61/118) (MFE +1.22%)
   - −1.0% : fill 30min 45% · séance 70% (105/159) · gap 16% · délai 5.5min · rebond 61% (60/105) (MFE +1.42%)
   - −1.5% : fill 30min 29% · séance 53% (78/159) · gap 9% · délai 20.1min · rebond 56% (42/78) (MFE +1.25%)
   - −2.0% : fill 30min 22% · séance 45% (68/159) · gap 7% · délai 29.4min · rebond 66% (40/68) (MFE +1.38%)
   - −3.0% : fill 30min 9% · séance 28% (44/159) · gap 4% · délai 124.2min · rebond 65% (29/44) (MFE +1.48%)
   - −4.0% : fill 30min 4% · séance 19% (26/159) · gap 2% · délai 289.1min · rebond 51% (15/26) (MFE +1.06%)
   - −5.0% : fill 30min 2% · séance 10% (15/159) · gap 2% · délai 201.3min · rebond 48% (8/15) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.59%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.69%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.65%) → stop au-delà de −1.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=464 jambes) : jambe baissière méd −1.15% (p90 −2.58%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 98% (47/48) · rebond 59% (24/47)
      · −2.0% : fill 80% (37/48) · rebond 72% (24/37)
      · −3.0% : fill 47% (26/48) · rebond 65% (18/26)
      · −4.0% : fill 34% (15/48) · rebond 54% (10/15)
      · −5.0% : fill 18% (9/48) · rebond 69% (7/9)
   - **flat** (50 séances) :
      · −1.0% : fill 77% (36/50) · rebond 72% (24/36)
      · −2.0% : fill 32% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 19% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 15% (6/50) · rebond 22% (1/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 42% (22/61) · rebond 50% (12/22)
      · −2.0% : fill 27% (14/61) · rebond 54% (7/14)
      · −3.0% : fill 19% (8/61) · rebond 83% (6/8)
      · −4.0% : fill 8% (3/61) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/61) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 66% si les 15 1res min sont vertes (85 cas) · 35% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 78% si début vert vs 26% si rouge (base 51% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.44% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +1.87% → **scale +1.2% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **26%** (continue à baisser 52%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.07%** (au-delà de la MAE q10 -5.07%), cible rebond +1.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.61% .. +3.16%] · haut q95 +3.85% · bas q05 -3.09%
   - 60min (n=160) : retour [-2.83% .. +2.95%] · haut q95 +4.1% · bas q05 -3.45%
   - 2h (n=160) : retour [-3.34% .. +2.94%] · haut q95 +4.16% · bas q05 -3.96%
   - 4h (n=160) : retour [-3.31% .. +3.09%] · haut q95 +4.55% · bas q05 -4.47%
   - 6h (n=160) : retour [-4.42% .. +3.57%] · haut q95 +4.55% · bas q05 -5.67%
   - session (n=160) : retour [-6.44% .. +4.09%] · haut q95 +4.79% · bas q05 -7.02%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.33 · part idiosyncratique 0.67
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 38.2  _(momentum baissier)_
- **ADX** : 30.3  _(tendance etablie)_
- **MACD** : hist -9.02  _(pas de croisement recent)_
- **BB** : %B 0.42 · largeur 36.3%
- **ATR** : 67.41 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.187  _(distribution)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 42.3  _(transition)_
- **MA** : MA20 1126.62 · MA50 1207.49 · MA200 1554.11  _(prix < MA20)_
- **Dist MA** : MA20 -2.9% · MA50 -9.4% · MA200 -29.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89963 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
