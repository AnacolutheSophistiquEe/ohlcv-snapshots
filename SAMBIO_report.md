# 207940

**Generated** : 2026-09-03T00:20:36.970299+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1501000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1501000.00 (+4.0% vs entrée) · entrée ₩1443875.00 · stop ₩1407778.12 · T1 ₩1462108.12 · R/R 0.51  
> ↳ P(T1 av. stop) 58 % · EV/risk -0.051 · ¼-Kelly 0.002 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1440228.38–₩1447521.62 (mid ₩1443875.00)
- Spot actuel : ₩1501000.00 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1407778.12 (stop swing_plan-based (-11.67%))
- Targets : T1 ₩1462108.12 · R/R 0.51 | T2 ₩1480341.24 · R/R 1.01 | T3 ₩1498574.36 · R/R 1.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1407778.12


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (11.67 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.67 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.298 % | p01 -2.673 % | pire -5.458 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2489** [0.189 ; 0.3171] _(largeur 12.8 pt, n_eff 173.1)_
   - swing : **0.3533** [0.3043 ; 0.4048] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3505** [0.3016 ; 0.4019] _(largeur 10.0 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.54 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.59 % contre 2.80 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.65 % vs -6.25 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3214** (β de hausse 0.2173, asymétrie 1.4791) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.051 | EV/share : ₩-1823.876 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 36 % | T3 11 %
- Kelly (position) : f* 0.008 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 60.1 | bear 34.2 | side 5.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→68% · +2.0%→45% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.12% (p90 6.65%) · excursion haute méd. +1.52% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.73% vs midi 0.749% vs clôture 0.913% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑1%/↓2% ; spike-down 52% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; mean-reverting — autocorr -0.071)_ ; drift intra méd. 0.119% ; recovery-V 37%
- **σ réalisé intraday** 2.582% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 35% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 1501250.0 (VA 1500250.0–1510250.0 ; dernier close 1510000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 43% · rebond 71% · **stop −2.99%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 41% (gap-down >1% 14% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.86% (p90 −2.28%) · haut méd +0.51% · range méd 1.46%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.9%) · haut méd +0.65% · range méd 1.91%
- Excursion ouverture 30min (n=160) : bas méd −1.18% (p90 −3.21%) · haut méd +0.84% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.5%) · haut méd +0.95% · range méd 2.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1520000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (112/159) · gap 25% · délai 0.3min · rebond 60% (56/112) (MFE +1.24%)
   - −1.0% : fill 30min 53% · séance 63% (90/159) · gap 14% · délai 1.1min · rebond 62% (45/90) (MFE +1.48%)
   - −1.5% : fill 30min 42% · séance 52% (73/159) · gap 8% · délai 2.5min · rebond 61% (37/73) (MFE +1.54%)
   - −2.0% : fill 30min 29% · séance 43% (60/159) · gap 6% · délai 4.8min · rebond 71% (35/60) (MFE +1.64%)
   - −3.0% : fill 30min 12% · séance 24% (36/159) · gap 3% · délai 28.1min · rebond 51% (18/36) (MFE +1.03%)
   - −4.0% : fill 30min 7% · séance 15% (20/159) · gap 3% · délai 52.1min · rebond 56% (11/20) (MFE +1.35%)
   - −5.0% : fill 30min 3% · séance 8% (11/159) · gap 3% · délai 116.7min · rebond 79% (8/11) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.15%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.14%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.07% (p90 −2.65%) · ~7.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 100% (42/43) · rebond 67% (23/42)
      · −2.0% : fill 77% (33/43) · rebond 76% (19/33)
      · −3.0% : fill 32% (18/43) · rebond 44% (9/18)
      · −4.0% : fill 23% (10/43) · rebond 59% (5/10)
      · −5.0% : fill 13% (6/43) · rebond 100% (6/6)
   - **flat** (48 séances) :
      · −1.0% : fill 64% (29/48) · rebond 40% (10/29)
      · −2.0% : fill 36% (14/48) · rebond 42% (6/14)
      · −3.0% : fill 31% (10/48) · rebond 60% (6/10)
      · −4.0% : fill 17% (6/48) · rebond 62% (4/6)
      · −5.0% : fill 7% (3/48) · rebond 52% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 33% (19/68) · rebond 75% (12/19)
      · −2.0% : fill 20% (13/68) · rebond 89% (10/13)
      · −3.0% : fill 12% (8/68) · rebond 53% (3/8)
      · −4.0% : fill 7% (4/68) · rebond 42% (2/4)
      · −5.0% : fill 4% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 69% si les 15 1res min sont vertes (55 cas) · 32% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 75% si début vert vs 27% si rouge (base 46% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **75%** · continue >prix actuel 42% ; creux résiduel méd -1.52% (q20 -2.04%) → **SL/trailing à −2.04%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.28% / q75 +2.25% → **scale +1.28% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=102) : edge inversé — récupère vert seulement **27%** (continue à baisser 50%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.58%** (au-delà de la MAE q10 -3.58%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.28% .. +3.1%] · haut q95 +3.29% · bas q05 -3.6%
   - 60min (n=160) : retour [-3.55% .. +2.61%] · haut q95 +3.45% · bas q05 -4.21%
   - 2h (n=160) : retour [-3.63% .. +3.33%] · haut q95 +4.28% · bas q05 -4.68%
   - 4h (n=160) : retour [-4.47% .. +2.94%] · haut q95 +4.82% · bas q05 -5.38%
   - 6h (n=160) : retour [-4.72% .. +3.6%] · haut q95 +4.82% · bas q05 -5.41%
   - session (n=160) : retour [-4.37% .. +3.26%] · haut q95 +4.82% · bas q05 -5.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.04%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.7  _(momentum baissier)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist -12452.682  _(bearish_recent)_
- **BB** : %B 0.17 · largeur 9.2%
- **ATR** : 49500.0 (40.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.204  _(accumulation)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 47.7  _(transition)_
- **MA** : MA20 1548800.0 · MA50 1467500.0 · MA200 1584801.57  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 +2.3% · MA200 -5.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (211255 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
