# RHM

**Generated** : 2026-07-06T21:35:44.934149+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €1130.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €1130.00 (+4.7% vs entrée) · entrée €1079.70 · stop €1054.15 · T1 €1130.80 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % · EV/risk -0.071 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.37% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1073.24–€1086.16 (mid €1079.70)
- Spot actuel : €1130.00 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : €1054.15 (stop swing_plan-based (-12.8%))
- Targets : T1 €1130.80 · R/R 2.0 | T2 €1153.55 · R/R 2.89 | T3 €1176.30 · R/R 3.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1054.15


## Edge, scénarios & sizing

- EV/risk : -0.071 | EV/share : €-1.814 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.0 | bear 5.0 | side 75.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=5, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=5, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→49% · +3.0%→29% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.65%) · excursion haute méd. +1.98% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.504% vs midi 0.89% vs clôture 1.008% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 54% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.101 ; neutre — autocorr 0.017)_ ; drift intra méd. -0.279% ; recovery-V 46%
- **σ réalisé intraday** 2.911% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 72% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 1098.4925 (VA 1092.5175–1102.0775 ; dernier close 1093.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 68% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 39% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.75% (p90 −1.68%) · haut méd +0.56% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.02%) · haut méd +0.73% · range méd 1.87%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.2%) · haut méd +0.91% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.09% (p90 −2.42%) · haut méd +1.01% · range méd 2.29%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1093.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 75% (118/159) · gap 27% · délai 0.3min · rebond 55% (61/118) (MFE +1.13%)
   - −1.0% : fill 30min 46% · séance 70% (105/159) · gap 16% · délai 5.6min · rebond 60% (60/105) (MFE +1.41%)
   - −1.5% : fill 30min 30% · séance 54% (78/159) · gap 8% · délai 18.2min · rebond 55% (42/78) (MFE +1.21%)
   - −2.0% : fill 30min 22% · séance 46% (68/159) · gap 7% · délai 30.3min · rebond 68% (41/68) (MFE +1.36%)
   - −3.0% : fill 30min 9% · séance 29% (44/159) · gap 4% · délai 121.5min · rebond 67% (29/44) (MFE +1.57%)
   - −4.0% : fill 30min 4% · séance 20% (26/159) · gap 2% · délai 259.1min · rebond 55% (15/26) (MFE +1.25%)
   - −5.0% : fill 30min 2% · séance 10% (14/159) · gap 2% · délai 205.6min · rebond 48% (7/14) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −1.59%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.67% (p90 −1.69%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.65%) → stop au-delà de −1.48% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=463 jambes) : jambe baissière méd −1.12% (p90 −2.62%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 98% (46/47) · rebond 60% (24/46)
      · −2.0% : fill 80% (36/47) · rebond 72% (24/36)
      · −3.0% : fill 47% (25/47) · rebond 65% (17/25)
      · −4.0% : fill 34% (14/47) · rebond 54% (9/14)
      · −5.0% : fill 18% (8/47) · rebond 69% (6/8)
   - **flat** (51 séances) :
      · −1.0% : fill 79% (37/51) · rebond 67% (24/37)
      · −2.0% : fill 36% (18/51) · rebond 71% (10/18)
      · −3.0% : fill 24% (11/51) · rebond 56% (6/11)
      · −4.0% : fill 22% (9/51) · rebond 38% (3/9)
      · −5.0% : fill 14% (6/51) · rebond 22% (1/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 42% (22/61) · rebond 50% (12/22)
      · −2.0% : fill 27% (14/61) · rebond 54% (7/14)
      · −3.0% : fill 19% (8/61) · rebond 83% (6/8)
      · −4.0% : fill 8% (3/61) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/61) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 66% si les 15 1res min sont vertes (85 cas) · 34% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 78% si début vert vs 25% si rouge (base 50% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.44% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +1.87% → **scale +1.2% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **25%** (continue à baisser 54%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.02%** (au-delà de la MAE q10 -5.02%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.6% .. +3.15%] · haut q95 +3.85% · bas q05 -3.07%
   - 60min (n=160) : retour [-2.8% .. +2.94%] · haut q95 +4.09% · bas q05 -3.44%
   - 2h (n=160) : retour [-3.26% .. +2.93%] · haut q95 +4.16% · bas q05 -3.91%
   - 4h (n=160) : retour [-3.3% .. +3.07%] · haut q95 +4.55% · bas q05 -4.44%
   - 6h (n=160) : retour [-4.39% .. +3.56%] · haut q95 +4.55% · bas q05 -5.63%
   - session (n=160) : retour [-6.37% .. +4.05%] · haut q95 +4.78% · bas q05 -7.0%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 48.6  _(neutre)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist 9.49  _(bullish_recent)_
- **BB** : %B 0.55 · largeur 35.4%
- **ATR** : 60.96 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.042  _(neutre)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 39.0  _(transition)_
- **MA** : MA20 1111.41 · MA50 1191.24 · MA200 1542.18  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 -5.1% · MA200 -26.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90045 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
