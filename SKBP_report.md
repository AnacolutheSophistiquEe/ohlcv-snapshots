# 326030

**Generated** : 2026-09-01T21:58:44.746733+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩89000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩89000.00 (+2.1% vs entrée) · entrée ₩87175.00 · stop ₩85495.11 · T1 ₩90534.78 · R/R 2.0  
> ↳ P(T1 av. stop) 10 % _(réel 5 s)_ · EV/risk 0.061 _(réel 5 s)_ (GBM -0.04) · ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.93% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩86898.30–₩87451.70 (mid ₩87175.00)
- Spot actuel : ₩89000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩85495.11 (stop swing_plan-based (-8.86%))
- Targets : T1 ₩90534.78 · R/R 2.0 | T2 ₩90923.82 · R/R 2.23 | T3 ₩91312.86 · R/R 2.46
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩85495.11


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.98 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.86 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 8.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.59 % | p01 -2.833 % | pire -5.539 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5073** [0.4332 ; 0.5811] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3633** [0.3139 ; 0.415] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3682** [0.3186 ; 0.42] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (38.5 pt), swing (45.7 pt), deep (35.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.07 %** | CVaR **-6.23 %** | vol 2.94 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.82 % contre 3.22 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.37 % vs -8.65 % si l'on extrapolait par √5 _(rapport 0.967 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6027** (β de hausse 0.4542, asymétrie 1.3269) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.04 | EV/share : ₩-67.040 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 17 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 18.5 | side 75.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.053% → cible +3.854% / stop −1.927%, p_fill 55%, n_eff≈21.1) : P(cible|rempli) **10%** · **EV/risk +0.061** (×p_fill ; si rempli +0.21% du capital)
  - **swing** (entrée dip −4.51% → cible +3.538% / stop −4.555%, p_fill 23%, n_eff≈11.1) : P(cible|rempli) **77%** · **EV/risk +0.085** (×p_fill ; si rempli +1.71% du capital)
  - **deep** (entrée dip −6.975% → cible +5.003% / stop −7.014%, p_fill 31%, n_eff≈14.1) : P(cible|rempli) **85%** · **EV/risk +0.146** (×p_fill ; si rempli +3.32% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→52% · +3.0%→36% · +5.0%→12% · +8.0%→6%
- Range intraday médian 4.48% (p90 8.26%) · excursion haute méd. +2.24% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.144% vs midi 0.991% vs clôture 0.972% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑1%/↓1% ; spike-down 62% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.112)_ ; drift intra méd. 0.147% ; recovery-V 30%
- **σ réalisé intraday** 3.279% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 48% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 87077.5 (VA 85747.5–87457.5 ; dernier close 87500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 75% · **stop −2.85%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 48% (gap-down >1% 20% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.36%) · haut méd +0.77% · range méd 2.05%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −2.97%) · haut méd +0.88% · range méd 2.46%
- Excursion ouverture 30min (n=160) : bas méd −1.16% (p90 −2.99%) · haut méd +1.14% · range méd 2.72%
- Excursion ouverture 60min (n=160) : bas méd −1.24% (p90 −3.19%) · haut méd +1.22% · range méd 2.97%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 87300.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (115/159) · gap 34% · délai 0.0min · rebond 49% (49/115) (MFE +0.97%)
   - −1.0% : fill 30min 56% · séance 70% (105/159) · gap 20% · délai 0.9min · rebond 55% (51/105) (MFE +1.14%)
   - −1.5% : fill 30min 44% · séance 60% (84/159) · gap 13% · délai 1.6min · rebond 70% (51/84) (MFE +1.41%)
   - −2.0% : fill 30min 35% · séance 47% (67/159) · gap 5% · délai 3.1min · rebond 67% (39/67) (MFE +1.61%)
   - −3.0% : fill 30min 19% · séance 38% (50/159) · gap 3% · délai 25.2min · rebond 57% (26/50) (MFE +1.53%)
   - −4.0% : fill 30min 10% · séance 23% (33/159) · gap 2% · délai 75.5min · rebond 75% (20/33) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 11% (19/159) · gap 1% · délai 126.3min · rebond 78% (11/19) (MFE +1.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.26% (p90 −2.15%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.5% (p90 −1.65%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −1.46%) → stop au-delà de −1.23% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=569 jambes) : jambe baissière méd −1.11% (p90 −2.43%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (55 séances) :
      · −1.0% : fill 93% (53/55) · rebond 60% (28/53)
      · −2.0% : fill 72% (40/55) · rebond 73% (24/40)
      · −3.0% : fill 64% (32/55) · rebond 64% (19/32)
      · −4.0% : fill 39% (22/55) · rebond 71% (13/22)
      · −5.0% : fill 18% (12/55) · rebond 79% (7/12)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 75% si les 15 1res min sont vertes (60 cas) · 23% si rouges (100 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **54min** → P(séance verte=clôture>ouverture) 83% si début vert vs 13% si rouge (base 44% · écart 69 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **83%** · continue >prix actuel 58% ; creux résiduel méd -1.65% (q20 -3.05%) → **SL/trailing à −3.05%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.53% / q75 +2.78% → **scale +1.53% / runner +2.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **13%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.4%** (au-delà de la MAE q10 -3.4%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +2.6%] · haut q95 +3.49% · bas q05 -3.95%
   - 60min (n=160) : retour [-3.01% .. +3.96%] · haut q95 +4.62% · bas q05 -4.13%
   - 2h (n=160) : retour [-3.42% .. +4.1%] · haut q95 +5.16% · bas q05 -4.23%
   - 4h (n=160) : retour [-3.61% .. +6.44%] · haut q95 +7.14% · bas q05 -5.22%
   - 6h (n=160) : retour [-4.47% .. +5.29%] · haut q95 +8.04% · bas q05 -5.64%
   - session (n=160) : retour [-4.55% .. +5.16%] · haut q95 +8.04% · bas q05 -5.64%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **volatil sans tendance propre (choppy)** (vol intra méd 2.63%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 47.3  _(neutre)_
- **ADX** : 15.7  _(pas de tendance nette)_
- **MACD** : hist 228.463  _(pas de croisement recent)_
- **BB** : %B 0.73 · largeur 13.2%
- **ATR** : 3871.43 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.128  _(accumulation)_
- **Vol ratio** : 0.98  _(volume normal)_
- **Choppiness** : 54.4  _(transition)_
- **MA** : MA20 86420.0 · MA50 83600.0 · MA200 103663.5  _(prix > MA20)_
- **Dist MA** : MA20 +3.0% · MA50 +6.5% · MA200 -14.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (500628 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
