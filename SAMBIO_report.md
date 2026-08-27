# 207940

**Generated** : 2026-08-27T00:22:19.885808+00:00  
**Santé technique** : 8/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1599000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1599000.00 (+0.7% vs entrée) · entrée ₩1588625.69 · stop ₩1461535.64 · T1 ₩1610137.47 · R/R 0.17  
> ↳ P(T1 av. stop) 51 % _(réel 5 s)_ · EV/risk -0.018 _(réel 5 s)_ (GBM -0.031) · ¼-Kelly 0.094 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1584323.34–₩1592928.05 (mid ₩1588625.69)
- Spot actuel : ₩1599000.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1461535.64 (stop swing_plan-based (-4.6%))
- Targets : T1 ₩1610137.47 · R/R 0.17 | T2 ₩1631649.24 · R/R 0.34 | T3 ₩1653161.01 · R/R 0.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1461535.64


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.49 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (4.6 %)** : le gap seul le franchit 0.247 % des séances (3 fois sur 1217).
   - exécution **0.631 pt plus bas** dans le cas TYPIQUE (médiane), 0.745 au p90, **0.773 au pire**
   - perte réelle **5.219 %** en moyenne _(tirée par la queue)_, jusqu'à **5.373 %** — au lieu des 4.6 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0015 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.277 % | p01 -2.575 % | pire -5.373 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.005** [0.0005 ; 0.0252] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.41** [0.3591 ; 0.4624] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.4152** [0.3641 ; 0.4677] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 36.8 observations effectives », dont la borne haute a 95 % vaut environ 8.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.3 pt), swing (32.7 pt), deep (31.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.95 %** | CVaR **-5.65 %** | vol 2.5 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.60 % contre 3.00 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.62 % vs -6.17 % si l'on extrapolait par √5 _(rapport 0.911 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3183** (β de hausse 0.2198, asymétrie 1.4484) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.031 | EV/share : ₩-3917.699 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 32 % | T3 10 %
- Kelly (position) : f* 0.375 | ¼-Kelly 0.094 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 32.6 | bear 61.4 | side 6.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.652% → cible +1.354% / stop −8.0%, p_fill 85%, n_eff≈36.8) : P(cible|rempli) **51%** · **EV/risk -0.018** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −1.424% → cible +3.028% / stop −3.222%, p_fill 79%, n_eff≈32.3) : P(cible|rempli) **59%** · **EV/risk +0.147** (×p_fill ; si rempli +0.60% du capital)
  - **deep** (entrée dip −2.206% → cible +4.282% / stop −4.872%, p_fill 70%, n_eff≈32.7) : P(cible|rempli) **65%** · **EV/risk +0.127** (×p_fill ; si rempli +0.88% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→62% · +2.0%→41% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.11% (p90 6.65%) · excursion haute méd. +1.37% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.681% vs midi 0.763% vs clôture 0.894% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (159 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 12% · trend ↑1%/↓2% ; spike-down 55% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; mean-reverting — autocorr -0.053)_ ; drift intra méd. -0.028% ; recovery-V 40%
- **σ réalisé intraday** 2.845% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 44% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 1545725.0 (VA 1540625.0–1563575.0 ; dernier close 1543000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 43% · rebond 72% · **stop −2.84%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.55 (high win-rate)
- Gaps overnight (n=158) : méd. 0.07% · baisse 38% (gap-down >1% 10% · >2% 5%)
- Excursion ouverture 5min (n=159) : bas méd −0.86% (p90 −2.4%) · haut méd +0.52% · range méd 1.47%
- Excursion ouverture 15min (n=159) : bas méd −1.1% (p90 −2.99%) · haut méd +0.66% · range méd 1.92%
- Excursion ouverture 30min (n=159) : bas méd −1.21% (p90 −3.38%) · haut méd +0.86% · range méd 2.34%
- Excursion ouverture 60min (n=159) : bas méd −1.27% (p90 −3.59%) · haut méd +0.92% · range méd 2.52%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1551000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 76% (107/158) · gap 22% · délai 0.3min · rebond 60% (52/107) (MFE +1.22%)
   - −1.0% : fill 30min 53% · séance 64% (88/158) · gap 10% · délai 1.4min · rebond 60% (42/88) (MFE +1.47%)
   - −1.5% : fill 30min 42% · séance 53% (72/158) · gap 7% · délai 2.7min · rebond 60% (37/72) (MFE +1.46%)
   - −2.0% : fill 30min 27% · séance 43% (59/158) · gap 5% · délai 6.1min · rebond 72% (35/59) (MFE +1.55%)
   - −3.0% : fill 30min 12% · séance 25% (36/158) · gap 1% · délai 32.6min · rebond 56% (19/36) (MFE +1.17%)
   - −4.0% : fill 30min 6% · séance 15% (19/158) · gap 1% · délai 65.7min · rebond 64% (11/19) (MFE +1.52%)
   - −5.0% : fill 30min 1% · séance 7% (10/158) · gap 1% · délai 173.8min · rebond 72% (7/10) (MFE +1.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −2.08%) → stop au-delà de −1.38% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.06%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=408 jambes) : jambe baissière méd −1.09% (p90 −2.74%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (40 séances) :
      · −1.0% : fill 99% (39/40) · rebond 65% (20/39)
      · −2.0% : fill 78% (31/40) · rebond 79% (18/31)
      · −3.0% : fill 34% (17/40) · rebond 53% (9/17)
      · −4.0% : fill 22% (9/40) · rebond 76% (5/9)
      · −5.0% : fill 10% (5/40) · rebond 100% (5/5)
   - **flat** (49 séances) :
      · −1.0% : fill 68% (29/49) · rebond 40% (10/29)
      · −2.0% : fill 38% (14/49) · rebond 42% (6/14)
      · −3.0% : fill 32% (10/49) · rebond 60% (6/10)
      · −4.0% : fill 18% (6/49) · rebond 62% (4/6)
      · −5.0% : fill 7% (3/49) · rebond 52% (1/3)
   - **gap-up** (69 séances) :
      · −1.0% : fill 36% (20/69) · rebond 74% (12/20)
      · −2.0% : fill 22% (14/69) · rebond 89% (11/14)
      · −3.0% : fill 14% (9/69) · rebond 54% (4/9)
      · −4.0% : fill 8% (4/69) · rebond 42% (2/4)
      · −5.0% : fill 4% (2/69) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=159) : 44% en base · 66% si les 15 1res min sont vertes (56 cas) · 31% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=159) : COUDE à **28min** → P(séance verte=clôture>ouverture) 79% si début vert vs 26% si rouge (base 44% · écart 53 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=53) : tient le vert **79%** · continue >prix actuel 44% ; creux résiduel méd -1.47% (q20 -2.53%) → **SL/trailing à −2.53%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.38% / q75 +2.57% → **scale +1.38% / runner +2.57%**, sortie à la clôture
  - **si ROUGE au coude** (n=106) : edge inversé — récupère vert seulement **26%** (continue à baisser 50%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.54%** (au-delà de la MAE q10 -3.54%), cible rebond +1.39% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=159) : retour [-3.33% .. +3.2%] · haut q95 +3.57% · bas q05 -4.02%
   - 60min (n=159) : retour [-3.57% .. +2.73%] · haut q95 +3.82% · bas q05 -4.25%
   - 2h (n=159) : retour [-3.84% .. +3.41%] · haut q95 +4.41% · bas q05 -4.69%
   - 4h (n=159) : retour [-4.89% .. +3.44%] · haut q95 +4.97% · bas q05 -5.42%
   - 6h (n=159) : retour [-4.73% .. +3.87%] · haut q95 +4.97% · bas q05 -5.99%
   - session (n=159) : retour [-4.57% .. +3.51%] · haut q95 +4.97% · bas q05 -6.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 65.9  _(momentum haussier)_
- **ADX** : 17.6  _(pas de tendance nette)_
- **MACD** : hist 298.806  _(bullish_recent)_
- **BB** : %B 0.83 · largeur 12.3%
- **ATR** : 50785.71 (47.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.21  _(accumulation)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 54.7  _(transition)_
- **MA** : MA20 1537350.0 · MA50 1451160.0 · MA200 1593639.85  _(prix > MA20)_
- **Dist MA** : MA20 +4.0% · MA50 +10.2% · MA200 +0.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (530508 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
