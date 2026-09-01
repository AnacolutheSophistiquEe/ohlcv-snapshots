# 326030

**Generated** : 2026-09-01T00:22:09.299901+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩87100.00  

> 🟡 **WAIT-FOR-DIP** — spot +3.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩87100.00 (+3.5% vs entrée) · entrée ₩84130.00 · stop ₩80208.57 · T1 ₩87111.69 · R/R 0.76  
> ↳ P(T1 av. stop) 62 % _(réel 5 s)_ · EV/risk 0.035 _(réel 5 s)_ (GBM -0.074) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩83533.66–₩84726.34 (mid ₩84130.00)
- Spot actuel : ₩87100.00 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : ₩80208.57 (stop swing_plan-based (-7.91%))
- Targets : T1 ₩87111.69 · R/R 0.76 | T2 ₩90093.39 · R/R 1.52 | T3 ₩93075.08 · R/R 2.28
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩80208.57


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.99 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (7.91 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 7.91 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.591 % | p01 -2.834 % | pire -5.539 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5025** [0.4285 ; 0.5764] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3596** [0.3103 ; 0.4112] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3693** [0.3197 ; 0.4211] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (37.9 pt), swing (42.1 pt), deep (33.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.07 %** | CVaR **-6.23 %** | vol 2.94 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.81 % contre 3.24 % aujourd'hui, rapport 0.56)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.37 % vs -8.66 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6027** (β de hausse 0.4535, asymétrie 1.329) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.074 | EV/share : ₩-291.612 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 26 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 29.6 | side 65.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.553% → cible +1.585% / stop −1.5%, p_fill 62%, n_eff≈24.1) : P(cible|rempli) **45%** · **EV/risk +0.110** (×p_fill ; si rempli +0.27% du capital)
  - **swing** (entrée dip −3.408% → cible +3.544% / stop −4.661%, p_fill 44%, n_eff≈18.0) : P(cible|rempli) **62%** · **EV/risk +0.035** (×p_fill ; si rempli +0.38% du capital)
  - **deep** (entrée dip −5.266% → cible +5.012% / stop −7.129%, p_fill 46%, n_eff≈19.3) : P(cible|rempli) **81%** · **EV/risk +0.183** (×p_fill ; si rempli +2.85% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→72% · +2.0%→52% · +3.0%→36% · +5.0%→12% · +8.0%→6%
- Range intraday médian 4.48% (p90 8.26%) · excursion haute méd. +2.24% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.133% vs midi 0.986% vs clôture 0.968% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 11% · trend ↑1%/↓1% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; mean-reverting — autocorr -0.098)_ ; drift intra méd. 0.117% ; recovery-V 25%
- **σ réalisé intraday** 3.248% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 50% / whipsaw 19%
- POC intraday (dernière séance, temps-au-prix) : 87136.25 (VA 86888.75–87466.25 ; dernier close 87900.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 22% · rebond 72% · **stop −3.37%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 47% (gap-down >1% 18% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.23%) · haut méd +0.82% · range méd 2.01%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.93%) · haut méd +0.89% · range méd 2.43%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −2.94%) · haut méd +1.14% · range méd 2.69%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.0%) · haut méd +1.32% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 88000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 77% (115/159) · gap 32% · délai 0.0min · rebond 50% (49/115) (MFE +1.05%)
   - −1.0% : fill 30min 55% · séance 69% (105/159) · gap 18% · délai 0.9min · rebond 56% (51/105) (MFE +1.21%)
   - −1.5% : fill 30min 43% · séance 59% (84/159) · gap 13% · délai 2.0min · rebond 69% (50/84) (MFE +1.41%)
   - −2.0% : fill 30min 34% · séance 46% (67/159) · gap 5% · délai 3.2min · rebond 65% (38/67) (MFE +1.77%)
   - −3.0% : fill 30min 18% · séance 36% (49/159) · gap 3% · délai 37.4min · rebond 55% (25/49) (MFE +1.44%)
   - −4.0% : fill 30min 8% · séance 22% (32/159) · gap 2% · délai 120.1min · rebond 72% (19/32) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 11% (19/159) · gap 1% · délai 126.3min · rebond 78% (11/19) (MFE +1.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −2.13%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.51% (p90 −1.65%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.46%) → stop au-delà de −1.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=569 jambes) : jambe baissière méd −1.11% (p90 −2.39%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 93% (53/55) · rebond 63% (28/53)
      · −2.0% : fill 71% (40/55) · rebond 71% (23/40)
      · −3.0% : fill 62% (31/55) · rebond 62% (18/31)
      · −4.0% : fill 36% (21/55) · rebond 67% (12/21)
      · −5.0% : fill 19% (12/55) · rebond 79% (7/12)
   - **flat** (38 séances) :
      · −1.0% : fill 72% (26/38) · rebond 38% (9/26)
      · −2.0% : fill 48% (16/38) · rebond 53% (9/16)
      · −3.0% : fill 38% (12/38) · rebond 28% (3/12)
      · −4.0% : fill 31% (9/38) · rebond 82% (6/9)
      · −5.0% : fill 17% (6/38) · rebond 80% (4/6)
   - **gap-up** (66 séances) :
      · −1.0% : fill 45% (26/66) · rebond 60% (14/26)
      · −2.0% : fill 20% (11/66) · rebond 65% (6/11)
      · −3.0% : fill 11% (6/66) · rebond 83% (4/6)
      · −4.0% : fill 2% (2/66) · rebond 71% (1/2)
      · −5.0% : fill 0% (1/66) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 75% si les 15 1res min sont vertes (60 cas) · 21% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **54min** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **83%** · continue >prix actuel 58% ; creux résiduel méd -1.65% (q20 -3.05%) → **SL/trailing à −3.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.53% / q75 +2.78% → **scale +1.53% / runner +2.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **11%** (continue à baisser 59%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.48%** (au-delà de la MAE q10 -3.48%), cible rebond +1.08% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +2.64%] · haut q95 +3.51% · bas q05 -4.0%
   - 60min (n=160) : retour [-3.02% .. +3.99%] · haut q95 +4.64% · bas q05 -4.15%
   - 2h (n=160) : retour [-3.44% .. +4.12%] · haut q95 +5.18% · bas q05 -4.25%
   - 4h (n=160) : retour [-3.64% .. +6.5%] · haut q95 +7.27% · bas q05 -5.32%
   - 6h (n=160) : retour [-4.48% .. +5.38%] · haut q95 +8.15% · bas q05 -5.72%
   - session (n=160) : retour [-4.57% .. +5.18%] · haut q95 +8.15% · bas q05 -5.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.62%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 47.1  _(neutre)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist 194.856  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 15.3%
- **ATR** : 3921.43 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.116  _(accumulation)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 54.9  _(transition)_
- **MA** : MA20 85880.0 · MA50 83556.0 · MA200 103815.0  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 +4.2% · MA200 -16.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (504203 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
