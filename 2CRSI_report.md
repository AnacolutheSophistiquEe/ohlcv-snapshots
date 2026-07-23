# AL2SI

**Generated** : 2026-07-23T00:09:19.361662+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €27.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)  
> ↳ spot €27.10 (+15.3% vs entrée) · entrée €23.51 · stop €22.36 · T1 €25.80 · R/R 1.99  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.31 · ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €23.05–€23.96 (mid €23.51)
- Spot actuel : €27.10 (+15.3% au-dessus de la zone — repli à attendre)
- Stop : €22.36 (stop swing_plan-based (-17.49%))
- Targets : T1 €25.80 · R/R 1.99 | T2 €28.09 · R/R 3.98 | T3 €30.38 · R/R 5.97
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.36


## Edge, scénarios & sizing

- EV/risk : 0.31 | EV/share : €0.355 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 20 % | T3 10 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 33.1 | bear 6.7 | side 60.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −6.022% → cible +4.357% / stop −4.488%, p_fill 42%, n_eff≈16.4) : P(cible|rempli) **27%** · **EV/risk -0.032** (×p_fill ; si rempli -0.34% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=7))
  - **deep** : indisponible (échantillon insuffisant (n=10, n_eff=9))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→74% · +3.0%→64% · +5.0%→41% · +8.0%→24%
- Range intraday médian 8.62% (p90 22.19%) · excursion haute méd. +4.16% / basse méd. −3.74%
- Profil de vol intra : ouverture 5.887% vs midi 1.768% vs clôture 2.01% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (153 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 9% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 37%)_
- **Régime intraday** : **chop** _(efficiency 0.141 ; mean-reverting — autocorr -0.042)_ ; drift intra méd. 0.275% ; recovery-V 34%
- **σ réalisé intraday** 8.413% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 28.982 (VA 28.246–28.982 ; dernier close 28.8)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 45% · rebond 92% · **stop −6.56%** sous le fill (sous le bruit) · cible +3.1% · R/R 0.47 (high win-rate)
- Gaps overnight (n=152) : méd. 0.16% · baisse 41% (gap-down >1% 23% · >2% 10%)
- Excursion ouverture 5min (n=153) : bas méd −1.25% (p90 −5.27%) · haut méd +1.03% · range méd 3.07%
- Excursion ouverture 15min (n=153) : bas méd −1.67% (p90 −5.86%) · haut méd +1.51% · range méd 4.55%
- Excursion ouverture 30min (n=153) : bas méd −1.75% (p90 −5.86%) · haut méd +2.15% · range méd 4.97%
- Excursion ouverture 60min (n=153) : bas méd −2.34% (p90 −6.96%) · haut méd +2.71% · range méd 6.15%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 28.8 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 82% (119/152) · gap 30% · délai 0.3min · rebond 70% (80/119) (MFE +3.34%)
   - −1.0% : fill 30min 64% · séance 80% (114/152) · gap 23% · délai 0.4min · rebond 73% (80/114) (MFE +2.82%)
   - −1.5% : fill 30min 56% · séance 76% (104/152) · gap 16% · délai 0.8min · rebond 73% (70/104) (MFE +2.21%)
   - −2.0% : fill 30min 48% · séance 68% (91/152) · gap 10% · délai 1.0min · rebond 71% (62/91) (MFE +2.01%)
   - −3.0% : fill 30min 36% · séance 57% (74/152) · gap 7% · délai 7.5min · rebond 86% (62/74) (MFE +2.37%)
   - −4.0% : fill 30min 29% · séance 49% (63/152) · gap 4% · délai 14.9min · rebond 76% (49/63) (MFE +3.07%)
   - −5.0% : fill 30min 21% · séance 45% (55/152) · gap 4% · délai 33.6min · rebond 92% (52/55) (MFE +3.1%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −5.56%) → stop au-delà de −3.71% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.32% (p90 −5.58%) → stop au-delà de −4.15% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.25% (p90 −5.69%) → stop au-delà de −4.0% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1486 jambes) : jambe baissière méd −1.25% (p90 −3.61%) · ~20.7 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 98% (50/54) · rebond 70% (34/50)
      · −2.0% : fill 88% (43/54) · rebond 60% (27/43)
      · −3.0% : fill 80% (38/54) · rebond 80% (31/38)
      · −4.0% : fill 70% (33/54) · rebond 77% (27/33)
      · −5.0% : fill 63% (30/54) · rebond 83% (27/30)
   - **flat** (33 séances) :
      · −1.0% : fill 85% (26/33) · rebond 84% (21/26)
      · −2.0% : fill 71% (20/33) · rebond 81% (15/20)
      · −3.0% : fill 55% (14/33) · rebond 95% (13/14)
      · −4.0% : fill 47% (13/33) · rebond 81% (11/13)
      · −5.0% : fill 41% (11/33) · rebond 100% (11/11)
   - **gap-up** (65 séances) :
      · −1.0% : fill 63% (38/65) · rebond 67% (25/38)
      · −2.0% : fill 50% (28/65) · rebond 79% (20/28)
      · −3.0% : fill 40% (22/65) · rebond 88% (18/22)
      · −4.0% : fill 34% (17/65) · rebond 72% (11/17)
      · −5.0% : fill 32% (14/65) · rebond 100% (14/14)
- **P(clôture VERTE) selon le drive 15min** (n=153) : 47% en base · 62% si les 15 1res min sont vertes (73 cas) · 36% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=153) : COUDE à **31min** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 47% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 252min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **73%** · continue >prix actuel 55% ; creux résiduel méd -2.63% (q20 -6.2%) → **SL/trailing à −6.2%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.87% / q75 +8.13% → **scale +3.87% / runner +8.13%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −10.63%** (au-delà de la MAE q10 -10.63%), cible rebond +2.32% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=153) : retour [-5.3% .. +6.79%] · haut q95 +8.67% · bas q05 -7.75%
   - 60min (n=153) : retour [-6.01% .. +9.43%] · haut q95 +9.95% · bas q05 -8.32%
   - 2h (n=153) : retour [-6.05% .. +10.12%] · haut q95 +11.47% · bas q05 -8.4%
   - 4h (n=153) : retour [-9.13% .. +10.42%] · haut q95 +12.76% · bas q05 -11.62%
   - 6h (n=153) : retour [-8.92% .. +14.51%] · haut q95 +17.57% · bas q05 -12.03%
   - session (n=153) : retour [-10.1% .. +17.94%] · haut q95 +18.85% · bas q05 -15.88%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — AL2SI = **volatil sans tendance propre (choppy)** (vol intra méd 5.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 28.7  _(survente)_
- **ADX** : 25.1  _(tendance etablie)_
- **MACD** : hist -0.066  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 59.7%
- **ATR** : 3.81 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.021  _(neutre)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 42.0  _(transition)_
- **MA** : MA20 30.67 · MA50 38.85 · MA200 24.29  _(prix < MA20)_
- **Dist MA** : MA20 -11.6% · MA50 -30.2% · MA200 +11.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90357 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
