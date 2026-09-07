# 326030

**Generated** : 2026-09-07T00:32:48.156737+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩86600.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩86600.00 (+1.4% vs entrée) · entrée ₩85375.00 · stop ₩84094.38 · T1 ₩86739.06 · R/R 1.07  
> ↳ P(T1 av. stop) 29 % _(réel 5 s)_ · EV/risk 0.041 _(réel 5 s)_ (GBM 0.023) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩85102.19–₩85647.81 (mid ₩85375.00)
- Spot actuel : ₩86600.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩84094.38 (stop swing_plan-based (-7.66%))
- Targets : T1 ₩86739.06 · R/R 1.07 | T2 ₩88103.12 · R/R 2.13 | T3 ₩89467.18 · R/R 3.2
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩84094.38


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.99 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (7.66 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 7.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.591 % | p01 -2.834 % | pire -5.539 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5112** [0.4371 ; 0.585] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.362** [0.3127 ; 0.4136] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3634** [0.314 ; 0.4151] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.1 pt), swing (40.3 pt), deep (32.2 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.07 %** | CVaR **-6.23 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.75 % contre 3.22 % aujourd'hui, rapport 0.54)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.34 % vs -8.66 % si l'on extrapolait par √5 _(rapport 0.963 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6036** (β de hausse 0.4508, asymétrie 1.3388) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.023 | EV/share : ₩29.111 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 27 % | T3 11 %
- Kelly (position) : f* 0.049 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 18.2 | side 75.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.411% → cible +1.598% / stop −1.5%, p_fill 68%, n_eff≈26.1) : P(cible|rempli) **29%** · **EV/risk +0.041** (×p_fill ; si rempli +0.09% du capital)
  - **swing** (entrée dip −3.107% → cible +3.573% / stop −4.699%, p_fill 51%, n_eff≈18.8) : P(cible|rempli) **67%** · **EV/risk +0.082** (×p_fill ; si rempli +0.75% du capital)
  - **deep** (entrée dip −4.811% → cible +5.052% / stop −7.174%, p_fill 46%, n_eff≈20.9) : P(cible|rempli) **81%** · **EV/risk +0.202** (×p_fill ; si rempli +3.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→71% · +2.0%→52% · +3.0%→35% · +5.0%→11% · +8.0%→6%
- Range intraday médian 4.45% (p90 8.26%) · excursion haute méd. +2.24% / basse méd. −2.27%
- Profil de vol intra : ouverture 3.076% vs midi 0.993% vs clôture 0.988% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑1%/↓1% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; mean-reverting — autocorr -0.113)_ ; drift intra méd. 0.129% ; recovery-V 25%
- **σ réalisé intraday** 3.137% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 55% / bas 53% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 86400.0 (VA 86320.0–86800.0 ; dernier close 86500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 75% · **stop −2.85%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 48% (gap-down >1% 20% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.29%) · haut méd +0.67% · range méd 1.9%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −2.94%) · haut méd +0.73% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.14% (p90 −2.97%) · haut méd +0.96% · range méd 2.66%
- Excursion ouverture 60min (n=160) : bas méd −1.2% (p90 −3.15%) · haut méd +1.21% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 86600.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (117/159) · gap 33% · délai 0.0min · rebond 48% (50/117) (MFE +0.97%)
   - −1.0% : fill 30min 53% · séance 69% (106/159) · gap 20% · délai 0.9min · rebond 54% (52/106) (MFE +1.14%)
   - −1.5% : fill 30min 43% · séance 60% (85/159) · gap 12% · délai 1.7min · rebond 72% (53/85) (MFE +1.41%)
   - −2.0% : fill 30min 34% · séance 45% (67/159) · gap 5% · délai 3.1min · rebond 68% (40/67) (MFE +1.58%)
   - −3.0% : fill 30min 18% · séance 37% (50/159) · gap 3% · délai 37.6min · rebond 55% (26/50) (MFE +1.45%)
   - −4.0% : fill 30min 9% · séance 22% (32/159) · gap 2% · délai 80.3min · rebond 75% (20/32) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 10% (18/159) · gap 1% · délai 127.0min · rebond 79% (11/18) (MFE +1.62%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −2.0%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.51% (p90 −1.57%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.51% (p90 −1.44%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=579 jambes) : jambe baissière méd −1.1% (p90 −2.38%) · ~9.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 90% (53/56) · rebond 57% (28/53)
      · −2.0% : fill 70% (40/56) · rebond 75% (25/40)
      · −3.0% : fill 62% (32/56) · rebond 60% (19/32)
      · −4.0% : fill 36% (21/56) · rebond 72% (13/21)
      · −5.0% : fill 16% (11/56) · rebond 80% (7/11)
   - **flat** (36 séances) :
      · −1.0% : fill 72% (26/36) · rebond 38% (9/26)
      · −2.0% : fill 49% (16/36) · rebond 53% (9/16)
      · −3.0% : fill 39% (12/36) · rebond 28% (3/12)
      · −4.0% : fill 31% (9/36) · rebond 82% (6/9)
      · −5.0% : fill 17% (6/36) · rebond 80% (4/6)
   - **gap-up** (67 séances) :
      · −1.0% : fill 45% (27/67) · rebond 64% (15/27)
      · −2.0% : fill 18% (11/67) · rebond 65% (6/11)
      · −3.0% : fill 10% (6/67) · rebond 83% (4/6)
      · −4.0% : fill 2% (2/67) · rebond 71% (1/2)
      · −5.0% : fill 0% (1/67) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 73% si les 15 1res min sont vertes (60 cas) · 22% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **54min** → P(séance verte=clôture>ouverture) 77% si début vert vs 13% si rouge (base 43% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **77%** · continue >prix actuel 55% ; creux résiduel méd -1.66% (q20 -3.14%) → **SL/trailing à −3.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.52% / q75 +2.63% → **scale +1.52% / runner +2.63%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **13%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.33%** (au-delà de la MAE q10 -3.33%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +2.48%] · haut q95 +3.57% · bas q05 -3.76%
   - 60min (n=160) : retour [-2.93% .. +3.84%] · haut q95 +4.53% · bas q05 -4.06%
   - 2h (n=160) : retour [-3.31% .. +3.99%] · haut q95 +4.95% · bas q05 -4.16%
   - 4h (n=160) : retour [-3.47% .. +5.99%] · haut q95 +6.77% · bas q05 -4.9%
   - 6h (n=160) : retour [-4.42% .. +4.81%] · haut q95 +7.63% · bas q05 -5.3%
   - session (n=160) : retour [-4.45% .. +5.11%] · haut q95 +7.63% · bas q05 -5.3%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.65%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.7  _(neutre)_
- **ADX** : 14.6  _(pas de tendance nette)_
- **MACD** : hist -145.05  _(bearish_recent)_
- **BB** : %B 0.43 · largeur 8.9%
- **ATR** : 3942.86 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.095  _(accumulation)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 55.1  _(transition)_
- **MA** : MA20 87120.0 · MA50 83700.0 · MA200 103185.0  _(prix < MA20)_
- **Dist MA** : MA20 -0.6% · MA50 +3.5% · MA200 -16.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (480264 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
