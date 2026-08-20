# 326030

**Generated** : 2026-08-20T20:08:15.879350+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩86200.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩86200.00 (+1.3% vs entrée) · entrée ₩85058.33 · stop ₩83782.46 · T1 ₩86166.08 · R/R 0.87  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.001 _(réel 5 s)_ (GBM -0.005) · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 7/10 élevée alors que : RSI 71.1 > 70 (surachat) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩84836.78–₩85279.88 (mid ₩85058.33)
- Spot actuel : ₩86200.00 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : ₩83782.46 (stop swing_plan-based (-7.1%))
- Targets : T1 ₩86166.08 · R/R 0.87 | T2 ₩87273.82 · R/R 1.74 | T3 ₩88381.57 · R/R 2.6
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩83782.46


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.98 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (7.1 %)** : le gap seul le franchit 0.0 % des séances ; quand il le franchit, l'exécution est **0.0 points plus bas** → perte réelle **— %** _(et non 7.1 %)_
- Chocs d'ouverture : p05 -1.578 % | p01 -2.833 % | pire -5.539 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0765** [0.0438 ; 0.1232] _(largeur 7.9 pt, n_eff 173.1)_
   - swing : **0.3825** [0.3324 ; 0.4345] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.5302** [0.4775 ; 0.5824] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.9 pt), swing (39.6 pt), deep (33.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.18 %** | CVaR **-6.25 %** | vol 2.92 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.90 % contre 3.47 % aujourd'hui, rapport 0.55)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.37 % vs -8.48 % si l'on extrapolait par √5 _(rapport 0.987 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6117** (β de hausse 0.4606, asymétrie 1.3282) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.005 | EV/share : ₩-6.614 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 36 % | T3 17 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.0 | bear 19.4 | side 74.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.32% → cible +1.302% / stop −1.5%, p_fill 66%, n_eff≈25.7) : P(cible|rempli) **48%** · **EV/risk -0.001** (×p_fill ; si rempli -0.00% du capital)
  - **swing** (entrée dip −2.915% → cible +2.912% / stop −4.31%, p_fill 44%, n_eff≈22.0) : P(cible|rempli) **48%** · **EV/risk -0.095** (×p_fill ; si rempli -0.94% du capital)
  - **deep** (entrée dip −4.503% → cible +4.118% / stop −6.573%, p_fill 49%, n_eff≈24.4) : P(cible|rempli) **74%** · **EV/risk +0.099** (×p_fill ; si rempli +1.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→70% · +2.0%→51% · +3.0%→36% · +5.0%→11% · +8.0%→5%
- Range intraday médian 4.47% (p90 7.69%) · excursion haute méd. +2.18% / basse méd. −2.27%
- Profil de vol intra : ouverture 2.979% vs midi 0.934% vs clôture 0.932% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (157 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 12% · trend ↑1%/↓1% ; spike-down 60% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.127)_ ; drift intra méd. 0.206% ; recovery-V 35%
- **σ réalisé intraday** 3.285% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 53% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 85028.75 (VA 84616.25–85358.75 ; dernier close 85200.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 46% · rebond 66% · **stop −3.5%** sous le fill (sous le bruit) · cible +1.56% · R/R 0.45 (high win-rate)
- Gaps overnight (n=156) : méd. 0.0% · baisse 45% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=157) : bas méd −0.75% (p90 −2.2%) · haut méd +0.76% · range méd 2.02%
- Excursion ouverture 15min (n=157) : bas méd −0.98% (p90 −2.91%) · haut méd +0.87% · range méd 2.31%
- Excursion ouverture 30min (n=157) : bas méd −1.1% (p90 −2.93%) · haut méd +1.13% · range méd 2.64%
- Excursion ouverture 60min (n=157) : bas méd −1.16% (p90 −2.99%) · haut méd +1.36% · range méd 2.94%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 85200.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 80% (116/156) · gap 26% · délai 0.3min · rebond 54% (52/116) (MFE +1.27%)
   - −1.0% : fill 30min 55% · séance 70% (104/156) · gap 17% · délai 1.6min · rebond 61% (53/104) (MFE +1.47%)
   - −1.5% : fill 30min 42% · séance 57% (80/156) · gap 10% · délai 2.9min · rebond 62% (43/80) (MFE +1.48%)
   - −2.0% : fill 30min 29% · séance 46% (65/156) · gap 6% · délai 8.0min · rebond 66% (38/65) (MFE +1.56%)
   - −3.0% : fill 30min 14% · séance 32% (42/156) · gap 2% · délai 50.0min · rebond 63% (20/42) (MFE +1.41%)
   - −4.0% : fill 30min 5% · séance 18% (27/156) · gap 2% · délai 126.2min · rebond 62% (14/27) (MFE +1.35%)
   - −5.0% : fill 30min 4% · séance 12% (20/156) · gap 2% · délai 139.7min · rebond 83% (13/20) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.36% (p90 −2.55%) → stop au-delà de −1.3% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.69%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.48%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=548 jambes) : jambe baissière méd −1.07% (p90 −2.38%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (48 séances) :
      · −1.0% : fill 96% (47/48) · rebond 66% (26/47)
      · −2.0% : fill 75% (34/48) · rebond 62% (18/34)
      · −3.0% : fill 50% (22/48) · rebond 70% (11/22)
      · −4.0% : fill 29% (16/48) · rebond 70% (9/16)
      · −5.0% : fill 19% (12/48) · rebond 85% (8/12)
   - **flat** (43 séances) :
      · −1.0% : fill 69% (30/43) · rebond 51% (13/30)
      · −2.0% : fill 40% (19/43) · rebond 77% (13/19)
      · −3.0% : fill 32% (12/43) · rebond 61% (6/12)
      · −4.0% : fill 24% (9/43) · rebond 50% (4/9)
      · −5.0% : fill 18% (7/43) · rebond 84% (5/7)
   - **gap-up** (65 séances) :
      · −1.0% : fill 49% (27/65) · rebond 62% (14/27)
      · −2.0% : fill 26% (12/65) · rebond 63% (7/12)
      · −3.0% : fill 17% (8/65) · rebond 47% (3/8)
      · −4.0% : fill 2% (2/65) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/65) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=157) : 45% en base · 73% si les 15 1res min sont vertes (58 cas) · 24% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=157) : COUDE à **54min** → P(séance verte=clôture>ouverture) 81% si début vert vs 12% si rouge (base 45% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 201min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **81%** · continue >prix actuel 55% ; creux résiduel méd -1.65% (q20 -3.12%) → **SL/trailing à −3.12%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.53% / q75 +2.59% → **scale +1.53% / runner +2.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **12%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.89%** (au-delà de la MAE q10 -3.89%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=157) : retour [-2.63% .. +2.86%] · haut q95 +3.62% · bas q05 -3.25%
   - 60min (n=157) : retour [-2.81% .. +4.13%] · haut q95 +5.04% · bas q05 -4.02%
   - 2h (n=157) : retour [-3.23% .. +4.28%] · haut q95 +5.35% · bas q05 -4.05%
   - 4h (n=157) : retour [-4.05% .. +4.93%] · haut q95 +6.22% · bas q05 -5.74%
   - 6h (n=157) : retour [-4.56% .. +4.31%] · haut q95 +6.94% · bas q05 -5.96%
   - session (n=157) : retour [-4.66% .. +4.76%] · haut q95 +6.94% · bas q05 -5.96%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.45%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 71.1  _(surachat)_
- **ADX** : 17.6  _(pas de tendance nette)_
- **MACD** : hist 526.431  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 20.5%
- **ATR** : 3607.14 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.102  _(accumulation)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 42.2  _(transition)_
- **MA** : MA20 83100.0 · MA50 83782.0 · MA200 104862.5  _(prix > MA20)_
- **Dist MA** : MA20 +3.7% · MA50 +2.9% · MA200 -17.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (402203 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
