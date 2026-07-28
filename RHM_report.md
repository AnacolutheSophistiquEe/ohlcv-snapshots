# RHM

**Generated** : 2026-07-28T21:36:04.724989+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €1086.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €1086.80 (+3.7% vs entrée) · entrée €1048.22 · stop €1027.26 · T1 €1064.83 · R/R 0.79  
> ↳ P(T1 av. stop) 51 % · EV/risk -0.008 · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 129 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1044.90–€1051.55 (mid €1048.22)
- Spot actuel : €1086.80 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : €1027.26 (stop swing_plan-based (-9.44%))
- Targets : T1 €1064.83 · R/R 0.79 | T2 €1081.43 · R/R 1.58 | T3 €1098.03 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1027.26


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : €-0.162 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 23 % | T3 3 %
- Kelly (position) : f* 0.042 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 78.0 | bear 5.0 | side 17.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.551% → cible +1.584% / stop −2.0%, p_fill 24%, n_eff≈11.7) : P(cible|rempli) **44%** · **EV/risk +0.046** (×p_fill ; si rempli +0.39% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=11, n_eff=6))
  - **deep** : indisponible (échantillon insuffisant (n=11, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→62% · +2.0%→46% · +3.0%→25% · +5.0%→1% · +8.0%→0%
- Range intraday médian 3.96% (p90 6.65%) · excursion haute méd. +1.72% / basse méd. −1.72%
- Profil de vol intra : ouverture 2.47% vs midi 0.844% vs clôture 1.081% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 51% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; mean-reverting — autocorr -0.033)_ ; drift intra méd. -0.148% ; recovery-V 45%
- **σ réalisé intraday** 2.69% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 76% / bas 62% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1048.8225 (VA 1043.2125–1058.1725 ; dernier close 1054.4)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 21% · rebond 60% · **stop −3.16%** sous le fill (sous le bruit) · cible +1.45% · R/R 0.46 (high win-rate)
- Gaps overnight (n=159) : méd. 0.09% · baisse 42% (gap-down >1% 12% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.72% (p90 −1.73%) · haut méd +0.63% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −1.99%) · haut méd +0.71% · range méd 1.85%
- Excursion ouverture 30min (n=160) : bas méd −0.98% (p90 −2.38%) · haut méd +0.88% · range méd 2.11%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.63%) · haut méd +1.0% · range méd 2.24%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1054.4 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 76% (120/159) · gap 28% · délai 0.3min · rebond 59% (64/120) (MFE +1.34%)
   - −1.0% : fill 30min 47% · séance 67% (108/159) · gap 12% · délai 4.4min · rebond 62% (64/108) (MFE +1.4%)
   - −1.5% : fill 30min 30% · séance 52% (80/159) · gap 6% · délai 18.1min · rebond 51% (42/80) (MFE +1.14%)
   - −2.0% : fill 30min 21% · séance 43% (69/159) · gap 5% · délai 30.4min · rebond 61% (42/69) (MFE +1.32%)
   - −3.0% : fill 30min 10% · séance 29% (45/159) · gap 2% · délai 119.5min · rebond 60% (27/45) (MFE +1.31%)
   - −4.0% : fill 30min 5% · séance 21% (27/159) · gap 2% · délai 152.8min · rebond 60% (15/27) (MFE +1.45%)
   - −5.0% : fill 30min 2% · séance 10% (15/159) · gap 1% · délai 201.2min · rebond 48% (7/15) (MFE +0.73%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −1.64%) → stop au-delà de −1.21% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −1.73%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.3% (p90 −1.75%) → stop au-delà de −1.57% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=468 jambes) : jambe baissière méd −1.06% (p90 −2.52%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 94% (49/51) · rebond 63% (28/49)
      · −2.0% : fill 77% (38/51) · rebond 64% (25/38)
      · −3.0% : fill 49% (26/51) · rebond 59% (16/26)
      · −4.0% : fill 36% (15/51) · rebond 70% (10/15)
      · −5.0% : fill 16% (8/51) · rebond 76% (6/8)
   - **flat** (50 séances) :
      · −1.0% : fill 67% (36/50) · rebond 69% (24/36)
      · −2.0% : fill 28% (17/50) · rebond 72% (10/17)
      · −3.0% : fill 19% (10/50) · rebond 55% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 36% (2/8)
      · −5.0% : fill 11% (6/50) · rebond 22% (1/6)
   - **gap-up** (58 séances) :
      · −1.0% : fill 41% (23/58) · rebond 49% (12/23)
      · −2.0% : fill 25% (14/58) · rebond 46% (7/14)
      · −3.0% : fill 19% (9/58) · rebond 66% (6/9)
      · −4.0% : fill 11% (4/58) · rebond 61% (3/4)
      · −5.0% : fill 4% (1/58) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 54% en base · 71% si les 15 1res min sont vertes (84 cas) · 38% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 79% si début vert vs 29% si rouge (base 54% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **79%** · continue >prix actuel 55% ; creux résiduel méd -0.94% (q20 -2.03%) → **SL/trailing à −2.03%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.35% / q75 +2.23% → **scale +1.35% / runner +2.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **29%** (continue à baisser 54%) → **RÉDUIRE ~71%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.58%** (au-delà de la MAE q10 -4.58%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.64% .. +3.02%] · haut q95 +3.74% · bas q05 -3.12%
   - 60min (n=160) : retour [-3.23% .. +2.99%] · haut q95 +3.9% · bas q05 -3.86%
   - 2h (n=160) : retour [-3.52% .. +2.77%] · haut q95 +4.04% · bas q05 -4.48%
   - 4h (n=160) : retour [-3.52% .. +2.87%] · haut q95 +4.4% · bas q05 -5.03%
   - 6h (n=160) : retour [-4.53% .. +3.06%] · haut q95 +4.53% · bas q05 -5.69%
   - session (n=160) : retour [-6.17% .. +4.13%] · haut q95 +4.74% · bas q05 -6.58%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.29%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.4  _(momentum haussier)_
- **ADX** : 23.3  _(pas de tendance nette)_
- **MACD** : hist 15.362  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 20.4%
- **ATR** : 41.09 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.094  _(accumulation)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 1031.67 · MA50 1112.62 · MA200 1469.43  _(prix > MA20)_
- **Dist MA** : MA20 +5.3% · MA50 -2.3% · MA200 -26.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89913 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
