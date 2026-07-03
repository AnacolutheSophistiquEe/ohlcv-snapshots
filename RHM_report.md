# RHM

**Generated** : 2026-07-03T00:02:13.284868+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · €1117.80  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €1117.80 (+6.0% vs entrée) · entrée €1054.19 · stop €1015.88 · T1 €1130.80 · R/R 2.0  
> ↳ P(T1 av. stop) 2 % · EV/risk -0.105 · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.63% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1047.93–€1060.44 (mid €1054.19)
- Spot actuel : €1117.80 (+6.0% au-dessus de la zone — repli à attendre)
- Stop : €1015.88 (stop swing_plan-based (-14.31%))
- Targets : T1 €1130.80 · R/R 2.0 | T2 €1139.29 · R/R 2.22 | T3 €1147.79 · R/R 2.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1015.88


## Edge, scénarios & sizing

- EV/risk : -0.105 | EV/share : €-4.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 2 % | T2 2 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.6 | bear 32.2 | side 58.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=4))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=2, n_eff=2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→64% · +2.0%→50% · +3.0%→30% · +5.0%→2% · +8.0%→0%
- Range intraday médian 4.15% (p90 6.53%) · excursion haute méd. +2.02% / basse méd. −1.66%
- Profil de vol intra : ouverture 2.537% vs midi 0.886% vs clôture 1.015% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 13% · trend ↑0%/↓0% ; spike-down 52% · recovery-V 39%)_
- **Régime intraday** : **chop** _(efficiency 0.093 ; neutre — autocorr 0.01)_ ; drift intra méd. -0.415% ; recovery-V 45%
- **σ réalisé intraday** 2.951% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 69% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 1029.0125 (VA 1027.5875–1046.1125 ; dernier close 1047.9)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −3.35%** sous le fill (sous le bruit) · cible +1.38% · R/R 0.41 (high win-rate)
- Gaps overnight (n=159) : méd. 0.08% · baisse 41% (gap-down >1% 17% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.7% (p90 −1.73%) · haut méd +0.57% · range méd 1.51%
- Excursion ouverture 15min (n=160) : bas méd −0.97% (p90 −1.96%) · haut méd +0.78% · range méd 1.88%
- Excursion ouverture 30min (n=160) : bas méd −1.03% (p90 −2.22%) · haut méd +0.99% · range méd 2.17%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −2.46%) · haut méd +1.01% · range méd 2.3%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1047.9 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 76% (119/159) · gap 28% · délai 0.3min · rebond 56% (61/119) (MFE +1.22%)
   - −1.0% : fill 30min 46% · séance 71% (106/159) · gap 17% · délai 5.5min · rebond 61% (60/106) (MFE +1.42%)
   - −1.5% : fill 30min 29% · séance 54% (79/159) · gap 9% · délai 20.0min · rebond 56% (42/79) (MFE +1.24%)
   - −2.0% : fill 30min 23% · séance 46% (69/159) · gap 7% · délai 29.0min · rebond 66% (41/69) (MFE +1.38%)
   - −3.0% : fill 30min 10% · séance 28% (45/159) · gap 4% · délai 122.8min · rebond 65% (30/45) (MFE +1.47%)
   - −4.0% : fill 30min 5% · séance 19% (27/159) · gap 2% · délai 287.1min · rebond 51% (15/27) (MFE +1.05%)
   - −5.0% : fill 30min 2% · séance 10% (16/159) · gap 2% · délai 197.1min · rebond 49% (9/16) (MFE +0.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.55% (p90 −1.37%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −1.62%) → stop au-delà de −1.35% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.27% (p90 −1.6%) → stop au-delà de −1.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=461 jambes) : jambe baissière méd −1.15% (p90 −2.61%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 98% (48/49) · rebond 59% (24/48)
      · −2.0% : fill 80% (38/49) · rebond 72% (25/38)
      · −3.0% : fill 47% (27/49) · rebond 65% (19/27)
      · −4.0% : fill 34% (16/49) · rebond 54% (10/16)
      · −5.0% : fill 19% (10/49) · rebond 70% (8/10)
   - **flat** (50 séances) :
      · −1.0% : fill 77% (36/50) · rebond 72% (24/36)
      · −2.0% : fill 32% (17/50) · rebond 65% (9/17)
      · −3.0% : fill 19% (10/50) · rebond 42% (5/10)
      · −4.0% : fill 17% (8/50) · rebond 16% (2/8)
      · −5.0% : fill 15% (6/50) · rebond 22% (1/6)
   - **gap-up** (60 séances) :
      · −1.0% : fill 44% (22/60) · rebond 50% (12/22)
      · −2.0% : fill 28% (14/60) · rebond 54% (7/14)
      · −3.0% : fill 20% (8/60) · rebond 83% (6/8)
      · −4.0% : fill 9% (3/60) · rebond 100% (3/3)
      · −5.0% : fill 0% (0/60) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 65% si les 15 1res min sont vertes (85 cas) · 35% si rouges (75 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:02** → P(séance verte=clôture>ouverture) 78% si début vert vs 23% si rouge (base 50% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 295min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=78) : tient le vert **78%** · continue >prix actuel 46% ; creux résiduel méd -1.44% (q20 -2.46%) → **SL/trailing à −2.46%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.2% / q75 +1.87% → **scale +1.2% / runner +1.87%**, sortie à la clôture
  - **si ROUGE au coude** (n=82) : edge inversé — récupère vert seulement **23%** (continue à baisser 54%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.15%** (au-delà de la MAE q10 -5.15%), cible rebond +1.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.62% .. +3.17%] · haut q95 +3.85% · bas q05 -3.1%
   - 60min (n=160) : retour [-2.84% .. +2.97%] · haut q95 +4.11% · bas q05 -3.45%
   - 2h (n=160) : retour [-3.38% .. +2.95%] · haut q95 +4.16% · bas q05 -3.98%
   - 4h (n=160) : retour [-3.31% .. +3.11%] · haut q95 +4.55% · bas q05 -4.48%
   - 6h (n=160) : retour [-4.46% .. +2.95%] · haut q95 +4.55% · bas q05 -5.68%
   - session (n=160) : retour [-6.51% .. +3.61%] · haut q95 +4.73% · bas q05 -7.05%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.28%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.9  _(momentum baissier)_
- **ADX** : 29.7  _(tendance etablie)_
- **MACD** : hist -1.626  _(pas de croisement recent)_
- **BB** : %B 0.49 · largeur 36.5%
- **ATR** : 63.61 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.105  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 40.6  _(transition)_
- **MA** : MA20 1121.02 · MA50 1200.88 · MA200 1549.85  _(prix < MA20)_
- **Dist MA** : MA20 -0.3% · MA50 -6.9% · MA200 -27.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88115 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
