# 326030

**Generated** : 2026-08-28T00:22:40.750316+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩88000.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩88000.00 (+1.8% vs entrée) · entrée ₩86408.33 · stop ₩84442.05 · T1 ₩90340.91 · R/R 2.0  
> ↳ P(T1 av. stop) 2 % _(réel 5 s)_ · EV/risk 0.013 _(réel 5 s)_ (GBM -0.106) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.28% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩86131.70–₩86684.97 (mid ₩86408.33)
- Spot actuel : ₩88000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩84442.05 (stop swing_plan-based (-8.52%))
- Targets : T1 ₩90340.91 · R/R 2.0 | T2 ₩90443.08 · R/R 2.05 | T3 ₩90545.25 · R/R 2.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩84442.05


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.99 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.52 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 8.52 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.591 % | p01 -2.834 % | pire -5.539 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4242** [0.3523 ; 0.4986] _(largeur 14.6 pt, n_eff 173.1)_
   - swing : **0.3592** [0.31 ; 0.4108] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3633** [0.3139 ; 0.415] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.3 pt), swing (44.6 pt), deep (31.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.18 %** | CVaR **-6.25 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.78 % contre 3.37 % aujourd'hui, rapport 0.53)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.37 % vs -8.66 % si l'on extrapolait par √5 _(rapport 0.966 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6034** (β de hausse 0.4573, asymétrie 1.3193) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.106 | EV/share : ₩-207.589 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 13 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.2 | bear 18.5 | side 75.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.806% → cible +4.551% / stop −2.276%, p_fill 58%, n_eff≈22.5) : P(cible|rempli) **2%** · **EV/risk +0.013** (×p_fill ; si rempli +0.05% du capital)
  - **swing** (entrée dip −3.983% → cible +3.568% / stop −4.725%, p_fill 30%, n_eff≈15.7) : P(cible|rempli) **62%** · **EV/risk +0.029** (×p_fill ; si rempli +0.46% du capital)
  - **deep** (entrée dip −6.154% → cible +5.047% / stop −7.252%, p_fill 34%, n_eff≈17.5) : P(cible|rempli) **86%** · **EV/risk +0.148** (×p_fill ; si rempli +3.14% du capital)
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
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 20% · rebond 77% · **stop −3.55%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.36 (high win-rate)
- Gaps overnight (n=158) : méd. 0.0% · baisse 48% (gap-down >1% 20% · >2% 6%)
- Excursion ouverture 5min (n=159) : bas méd −0.75% (p90 −2.19%) · haut méd +0.76% · range méd 1.98%
- Excursion ouverture 15min (n=159) : bas méd −1.07% (p90 −2.81%) · haut méd +0.86% · range méd 2.32%
- Excursion ouverture 30min (n=159) : bas méd −1.12% (p90 −2.93%) · haut méd +1.13% · range méd 2.64%
- Excursion ouverture 60min (n=159) : bas méd −1.21% (p90 −2.99%) · haut méd +1.21% · range méd 2.96%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 83700.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (116/158) · gap 33% · délai 0.0min · rebond 54% (50/116) (MFE +1.24%)
   - −1.0% : fill 30min 54% · séance 70% (106/158) · gap 20% · délai 0.9min · rebond 57% (51/106) (MFE +1.25%)
   - −1.5% : fill 30min 42% · séance 59% (82/158) · gap 14% · délai 1.7min · rebond 68% (48/82) (MFE +1.41%)
   - −2.0% : fill 30min 33% · séance 46% (66/158) · gap 6% · délai 3.2min · rebond 66% (37/66) (MFE +1.76%)
   - −3.0% : fill 30min 18% · séance 36% (47/158) · gap 4% · délai 37.4min · rebond 61% (25/47) (MFE +1.62%)
   - −4.0% : fill 30min 7% · séance 20% (30/158) · gap 2% · délai 120.0min · rebond 77% (18/30) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 12% (19/158) · gap 1% · délai 126.3min · rebond 78% (11/19) (MFE +1.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.34% (p90 −2.5%) → stop au-delà de −1.29% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.69%) → stop au-delà de −1.25% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.55% (p90 −1.48%) → stop au-delà de −1.28% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=556 jambes) : jambe baissière méd −1.09% (p90 −2.38%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 93% (53/55) · rebond 67% (28/53)
      · −2.0% : fill 69% (40/55) · rebond 68% (22/40)
      · −3.0% : fill 59% (30/55) · rebond 67% (18/30)
      · −4.0% : fill 33% (20/55) · rebond 78% (12/20)
      · −5.0% : fill 20% (12/55) · rebond 79% (7/12)
   - **flat** (38 séances) :
      · −1.0% : fill 70% (26/38) · rebond 42% (10/26)
      · −2.0% : fill 44% (15/38) · rebond 62% (9/15)
      · −3.0% : fill 33% (11/38) · rebond 34% (3/11)
      · −4.0% : fill 25% (8/38) · rebond 76% (5/8)
      · −5.0% : fill 18% (6/38) · rebond 80% (4/6)
   - **gap-up** (65 séances) :
      · −1.0% : fill 47% (27/65) · rebond 54% (13/27)
      · −2.0% : fill 23% (11/65) · rebond 65% (6/11)
      · −3.0% : fill 13% (6/65) · rebond 83% (4/6)
      · −4.0% : fill 2% (2/65) · rebond 71% (1/2)
      · −5.0% : fill 1% (1/65) · rebond 0% (0/1)
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
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 57.1  _(momentum haussier)_
- **ADX** : 15.9  _(pas de tendance nette)_
- **MACD** : hist 369.115  _(pas de croisement recent)_
- **BB** : %B 0.69 · largeur 18.6%
- **ATR** : 3992.86 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.15  _(accumulation)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 84955.0 · MA50 83636.0 · MA200 104144.0  _(prix > MA20)_
- **Dist MA** : MA20 +3.6% · MA50 +5.2% · MA200 -15.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (564951 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
