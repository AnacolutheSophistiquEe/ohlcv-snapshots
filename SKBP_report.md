# 326030

**Generated** : 2026-08-24T00:21:43.141680+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩83700.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩83700.00 (+1.4% vs entrée) · entrée ₩82563.33 · stop ₩78863.33 · T1 ₩85005.58 · R/R 0.66  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.173 _(réel 5 s)_ (GBM -0.102) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩82074.88–₩83051.78 (mid ₩82563.33)
- Spot actuel : ₩83700.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩78863.33 (stop swing_plan-based (-5.78%))
- Targets : T1 ₩85005.58 · R/R 0.66 | T2 ₩87447.83 · R/R 1.32 | T3 ₩89890.08 · R/R 1.98
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩78863.33


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.99 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (5.78 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 5.78 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.591 % | p01 -2.834 % | pire -5.539 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0756** [0.0431 ; 0.1221] _(largeur 7.9 pt, n_eff 173.1)_
   - swing : **0.3861** [0.3359 ; 0.4382] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.5271** [0.4744 ; 0.5793] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.0 pt), swing (34.3 pt), deep (31.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.53 %** | CVaR **-6.33 %** | vol 2.85 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 2.17 % contre 3.48 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.37 % vs -8.49 % si l'on extrapolait par √5 _(rapport 0.986 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6117** (β de hausse 0.4546, asymétrie 1.3456) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.102 | EV/share : ₩-376.550 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 30 % | T3 15 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈207) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.4 | bear 30.3 | side 64.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.619% → cible +1.323% / stop −1.5%, p_fill 82%, n_eff≈32.3) : P(cible|rempli) **55%** · **EV/risk +0.029** (×p_fill ; si rempli +0.05% du capital)
  - **swing** (entrée dip −1.36% → cible +2.958% / stop −4.481%, p_fill 73%, n_eff≈30.1) : P(cible|rempli) **48%** · **EV/risk -0.173** (×p_fill ; si rempli -1.07% du capital)
  - **deep** (entrée dip −2.099% → cible +4.183% / stop −6.773%, p_fill 71%, n_eff≈32.2) : P(cible|rempli) **66%** · **EV/risk +0.053** (×p_fill ; si rempli +0.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→71% · +2.0%→51% · +3.0%→36% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.47% (p90 7.69%) · excursion haute méd. +2.18% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.022% vs midi 0.946% vs clôture 0.952% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 61% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.106)_ ; drift intra méd. 0.017% ; recovery-V 31%
- **σ réalisé intraday** 3.232% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 82187.5 (VA 82037.5–83312.5 ; dernier close 83200.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 19% · rebond 65% · **stop −3.54%** sous le fill (sous le bruit) · cible +1.5% · R/R 0.42 (high win-rate)
- Gaps overnight (n=158) : méd. 0.0% · baisse 46% (gap-down >1% 18% · >2% 6%)
- Excursion ouverture 5min (n=159) : bas méd −0.75% (p90 −2.19%) · haut méd +0.76% · range méd 1.98%
- Excursion ouverture 15min (n=159) : bas méd −1.07% (p90 −2.81%) · haut méd +0.86% · range méd 2.32%
- Excursion ouverture 30min (n=159) : bas méd −1.12% (p90 −2.93%) · haut méd +1.13% · range méd 2.64%
- Excursion ouverture 60min (n=159) : bas méd −1.21% (p90 −2.99%) · haut méd +1.21% · range méd 2.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 83200.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 79% (117/158) · gap 26% · délai 0.2min · rebond 53% (52/117) (MFE +1.19%)
   - −1.0% : fill 30min 55% · séance 70% (105/158) · gap 18% · délai 1.4min · rebond 59% (53/105) (MFE +1.42%)
   - −1.5% : fill 30min 42% · séance 57% (81/158) · gap 10% · délai 1.8min · rebond 60% (43/81) (MFE +1.42%)
   - −2.0% : fill 30min 30% · séance 46% (66/158) · gap 6% · délai 5.6min · rebond 64% (38/66) (MFE +1.54%)
   - −3.0% : fill 30min 15% · séance 33% (43/158) · gap 2% · délai 41.2min · rebond 59% (20/43) (MFE +1.4%)
   - −4.0% : fill 30min 5% · séance 19% (28/158) · gap 2% · délai 123.0min · rebond 65% (15/28) (MFE +1.5%)
   - −5.0% : fill 30min 4% · séance 12% (20/158) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.5%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.69%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.48%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=556 jambes) : jambe baissière méd −1.09% (p90 −2.38%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 96% (48/49) · rebond 62% (26/48)
      · −2.0% : fill 76% (35/49) · rebond 58% (18/35)
      · −3.0% : fill 52% (23/49) · rebond 62% (11/23)
      · −4.0% : fill 33% (17/49) · rebond 76% (10/17)
      · −5.0% : fill 18% (12/49) · rebond 85% (8/12)
   - **flat** (43 séances) :
      · −1.0% : fill 69% (30/43) · rebond 51% (13/30)
      · −2.0% : fill 40% (19/43) · rebond 77% (13/19)
      · −3.0% : fill 32% (12/43) · rebond 61% (6/12)
      · −4.0% : fill 24% (9/43) · rebond 50% (4/9)
      · −5.0% : fill 18% (7/43) · rebond 84% (5/7)
   - **gap-up** (66 séances) :
      · −1.0% : fill 47% (27/66) · rebond 62% (14/27)
      · −2.0% : fill 25% (12/66) · rebond 63% (7/12)
      · −3.0% : fill 16% (8/66) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/66) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/66) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 43% en base · 73% si les 15 1res min sont vertes (58 cas) · 23% si rouges (101 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=159) : COUDE à **54min** → P(séance verte=clôture>ouverture) 81% si début vert vs 12% si rouge (base 43% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **81%** · continue >prix actuel 55% ; creux résiduel méd -1.65% (q20 -3.12%) → **SL/trailing à −3.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.53% / q75 +2.59% → **scale +1.53% / runner +2.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=97) : edge inversé — récupère vert seulement **12%** (continue à baisser 62%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.73%** (au-delà de la MAE q10 -3.73%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-2.62% .. +2.8%] · haut q95 +3.59% · bas q05 -3.23%
   - 60min (n=159) : retour [-2.74% .. +4.1%] · haut q95 +4.9% · bas q05 -3.97%
   - 2h (n=159) : retour [-3.23% .. +4.23%] · haut q95 +5.28% · bas q05 -4.04%
   - 4h (n=159) : retour [-3.84% .. +4.64%] · haut q95 +6.15% · bas q05 -5.69%
   - 6h (n=159) : retour [-4.53% .. +4.29%] · haut q95 +6.82% · bas q05 -5.92%
   - session (n=159) : retour [-4.64% .. +4.64%] · haut q95 +6.82% · bas q05 -5.92%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.48%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 60.6  _(momentum haussier)_
- **ADX** : 16.6  _(pas de tendance nette)_
- **MACD** : hist 258.869  _(pas de croisement recent)_
- **BB** : %B 0.52 · largeur 20.1%
- **ATR** : 3700.0 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.076  _(accumulation)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 83315.0 · MA50 83734.0 · MA200 104703.0  _(prix > MA20)_
- **Dist MA** : MA20 +0.5% · MA50 -0.0% · MA200 -20.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (752339 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
