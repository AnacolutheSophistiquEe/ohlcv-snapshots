# RHM

**Generated** : 2026-07-08T00:02:04.705824+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €1113.60  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €1113.60 (+4.3% vs entrée) · entrée €1067.40 · stop €1035.70 · T1 €1130.80 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % · EV/risk -0.081 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.97% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1061.01–€1073.79 (mid €1067.40)
- Spot actuel : €1113.60 (+4.3% au-dessus de la zone — repli à attendre)
- Stop : €1035.70 (stop swing_plan-based (-12.16%))
- Targets : T1 €1130.80 · R/R 2.0 | T2 €1146.86 · R/R 2.51 | T3 €1162.92 · R/R 3.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1035.70


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : €-2.567 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 4 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 22.8 | bear 5.0 | side 72.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.154% → cible +5.94% / stop −2.97%, p_fill 24%, n_eff≈9.2) : P(cible|rempli) **14%** · **EV/risk +0.061** (×p_fill ; si rempli +0.75% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=6, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=6, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→62% · +2.0%→49% · +3.0%→30% · +5.0%→4% · +8.0%→0%
- Range intraday médian 4.16% (p90 6.65%) · excursion haute méd. +1.98% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.527% vs midi 0.888% vs clôture 1.017% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 53% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; neutre — autocorr 0.024)_ ; drift intra méd. -0.071% ; recovery-V 46%
- **σ réalisé intraday** 2.892% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 69% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 1114.8725 (VA 1111.4675–1120.5475 ; dernier close 1133.6)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 45% · rebond 68% · **stop −3.14%** sous le fill (sous le bruit) · cible +1.36% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 40% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.71% (p90 −1.65%) · haut méd +0.57% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −0.98% (p90 −2.01%) · haut méd +0.74% · range méd 1.9%
- Excursion ouverture 30min (n=160) : bas méd −1.07% (p90 −2.19%) · haut méd +0.96% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −2.42%) · haut méd +1.01% · range méd 2.32%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1133.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 75% (118/159) · gap 28% · délai 0.3min · rebond 56% (61/118) (MFE +1.22%)
   - −1.0% : fill 30min 45% · séance 69% (105/159) · gap 16% · délai 5.6min · rebond 60% (60/105) (MFE +1.41%)
   - −1.5% : fill 30min 29% · séance 53% (78/159) · gap 8% · délai 18.2min · rebond 55% (42/78) (MFE +1.21%)
   - −2.0% : fill 30min 22% · séance 45% (68/159) · gap 7% · délai 30.3min · rebond 68% (41/68) (MFE +1.36%)
   - −3.0% : fill 30min 9% · séance 28% (44/159) · gap 4% · délai 121.5min · rebond 67% (29/44) (MFE +1.57%)
   - −4.0% : fill 30min 4% · séance 20% (26/159) · gap 2% · délai 259.1min · rebond 55% (15/26) (MFE +1.25%)
   - −5.0% : fill 30min 2% · séance 10% (14/159) · gap 2% · délai 205.6min · rebond 48% (7/14) (MFE +0.74%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.58%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.67%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −1.64%) → stop au-delà de −1.37% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=461 jambes) : jambe baissière méd −1.11% (p90 −2.6%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 92% (46/48) · rebond 60% (24/46)
      · −2.0% : fill 75% (36/48) · rebond 72% (24/36)
      · −3.0% : fill 44% (25/48) · rebond 65% (17/25)
      · −4.0% : fill 32% (14/48) · rebond 54% (9/14)
      · −5.0% : fill 17% (8/48) · rebond 69% (6/8)
   - **flat** (50 séances) :
      · −1.0% : fill 79% (37/50) · rebond 67% (24/37)
      · −2.0% : fill 36% (18/50) · rebond 71% (10/18)
      · −3.0% : fill 24% (11/50) · rebond 56% (6/11)
      · −4.0% : fill 22% (9/50) · rebond 38% (3/9)
      · −5.0% : fill 14% (6/50) · rebond 22% (1/6)
   - **gap-up** (61 séances) :
      · −1.0% : fill 42% (22/61) · rebond 50% (12/22)
      · −2.0% : fill 27% (14/61) · rebond 54% (7/14)
      · −3.0% : fill 19% (8/61) · rebond 83% (6/8)
      · −4.0% : fill 8% (3/61) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/61) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 67% si les 15 1res min sont vertes (85 cas) · 34% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 79% si début vert vs 25% si rouge (base 51% · écart 54 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **79%** · continue >prix actuel 48% ; creux résiduel méd -1.37% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.19% / q75 +1.87% → **scale +1.19% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **25%** (continue à baisser 54%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.02%** (au-delà de la MAE q10 -5.02%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.59% .. +3.15%] · haut q95 +3.84% · bas q05 -3.05%
   - 60min (n=160) : retour [-2.79% .. +3.12%] · haut q95 +4.08% · bas q05 -3.43%
   - 2h (n=160) : retour [-3.23% .. +2.92%] · haut q95 +4.16% · bas q05 -3.87%
   - 4h (n=160) : retour [-3.3% .. +3.05%] · haut q95 +4.55% · bas q05 -4.43%
   - 6h (n=160) : retour [-4.36% .. +3.54%] · haut q95 +4.55% · bas q05 -5.61%
   - session (n=160) : retour [-6.29% .. +4.3%] · haut q95 +4.78% · bas q05 -6.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 44.7  _(momentum baissier)_
- **ADX** : 24.4  _(pas de tendance nette)_
- **MACD** : hist 12.196  _(bullish_recent)_
- **BB** : %B 0.52 · largeur 34.6%
- **ATR** : 60.63 (49.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.066  _(distribution)_
- **Vol ratio** : 0.39  _(volume atone)_
- **Choppiness** : 38.8  _(transition)_
- **MA** : MA20 1106.73 · MA50 1186.86 · MA200 1538.24  _(prix > MA20)_
- **Dist MA** : MA20 +0.6% · MA50 -6.2% · MA200 -27.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90760 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
