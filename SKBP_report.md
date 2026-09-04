# 326030

**Generated** : 2026-09-04T00:23:39.519602+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩86400.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩86400.00 (+1.4% vs entrée) · entrée ₩85225.00 · stop ₩83946.62 · T1 ₩86597.30 · R/R 1.07  
> ↳ P(T1 av. stop) 37 % _(réel 5 s)_ · EV/risk -0.009 _(réel 5 s)_ (GBM 0.067) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩84950.54–₩85499.46 (mid ₩85225.00)
- Spot actuel : ₩86400.00 (+1.4% au-dessus de la zone — repli à attendre)
- Stop : ₩83946.62 (stop swing_plan-based (-7.64%))
- Targets : T1 ₩86597.30 · R/R 1.07 | T2 ₩87969.61 · R/R 2.15 | T3 ₩89341.91 · R/R 3.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩83946.62


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.99 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (7.64 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 7.64 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.591 % | p01 -2.834 % | pire -5.539 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5122** [0.4381 ; 0.5859] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3533** [0.3043 ; 0.4048] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3552** [0.3061 ; 0.4067] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (35.5 pt), swing (40.7 pt), deep (33.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.07 %** | CVaR **-6.23 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.76 % contre 3.22 % aujourd'hui, rapport 0.55)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.34 % vs -8.66 % si l'on extrapolait par √5 _(rapport 0.963 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6037** (β de hausse 0.451, asymétrie 1.3386) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : 0.067 | EV/share : ₩86.177 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 53 % | T2 29 % | T3 12 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 18.2 | side 76.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.36% → cible +1.61% / stop −1.5%, p_fill 66%, n_eff≈26.7) : P(cible|rempli) **37%** · **EV/risk -0.009** (×p_fill ; si rempli -0.02% du capital)
  - **swing** (entrée dip −2.994% → cible +3.601% / stop −4.789%, p_fill 48%, n_eff≈19.5) : P(cible|rempli) **62%** · **EV/risk +0.069** (×p_fill ; si rempli +0.69% du capital)
  - **deep** (entrée dip −4.621% → cible +5.092% / stop −7.307%, p_fill 49%, n_eff≈21.2) : P(cible|rempli) **80%** · **EV/risk +0.197** (×p_fill ; si rempli +2.94% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→72% · +2.0%→54% · +3.0%→38% · +5.0%→12% · +8.0%→6%
- Range intraday médian 4.48% (p90 8.26%) · excursion haute méd. +2.28% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.161% vs midi 0.994% vs clôture 0.975% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 10% · trend ↑1%/↓1% ; spike-down 61% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.12 ; mean-reverting — autocorr -0.099)_ ; drift intra méd. 0.279% ; recovery-V 30%
- **σ réalisé intraday** 3.272% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 45% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 89407.5 (VA 88982.5–89662.5 ; dernier close 89500.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 23% · rebond 75% · **stop −2.85%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 49% (gap-down >1% 19% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.77% (p90 −2.34%) · haut méd +0.8% · range méd 2.01%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.96%) · haut méd +0.89% · range méd 2.51%
- Excursion ouverture 30min (n=160) : bas méd −1.14% (p90 −2.99%) · haut méd +1.14% · range méd 2.73%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.18%) · haut méd +1.33% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 89000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (115/159) · gap 33% · délai 0.0min · rebond 49% (49/115) (MFE +0.97%)
   - −1.0% : fill 30min 55% · séance 69% (105/159) · gap 19% · délai 0.9min · rebond 55% (51/105) (MFE +1.14%)
   - −1.5% : fill 30min 44% · séance 59% (84/159) · gap 13% · délai 1.6min · rebond 70% (51/84) (MFE +1.41%)
   - −2.0% : fill 30min 35% · séance 46% (67/159) · gap 5% · délai 3.1min · rebond 67% (39/67) (MFE +1.61%)
   - −3.0% : fill 30min 19% · séance 37% (50/159) · gap 3% · délai 25.2min · rebond 57% (26/50) (MFE +1.53%)
   - −4.0% : fill 30min 10% · séance 23% (33/159) · gap 2% · délai 75.5min · rebond 75% (20/33) (MFE +1.28%)
   - −5.0% : fill 30min 3% · séance 11% (19/159) · gap 1% · délai 126.3min · rebond 78% (11/19) (MFE +1.6%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.24% (p90 −2.01%) → stop au-delà de −1.2% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.61%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.51% (p90 −1.44%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=570 jambes) : jambe baissière méd −1.09% (p90 −2.41%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (56 séances) :
      · −1.0% : fill 89% (53/56) · rebond 60% (28/53)
      · −2.0% : fill 69% (40/56) · rebond 73% (24/40)
      · −3.0% : fill 61% (32/56) · rebond 64% (19/32)
      · −4.0% : fill 38% (22/56) · rebond 71% (13/22)
      · −5.0% : fill 17% (12/56) · rebond 79% (7/12)
   - **flat** (37 séances) :
      · −1.0% : fill 72% (26/37) · rebond 38% (9/26)
      · −2.0% : fill 49% (16/37) · rebond 53% (9/16)
      · −3.0% : fill 38% (12/37) · rebond 28% (3/12)
      · −4.0% : fill 31% (9/37) · rebond 82% (6/9)
      · −5.0% : fill 17% (6/37) · rebond 80% (4/6)
   - **gap-up** (66 séances) :
      · −1.0% : fill 45% (26/66) · rebond 60% (14/26)
      · −2.0% : fill 20% (11/66) · rebond 65% (6/11)
      · −3.0% : fill 11% (6/66) · rebond 83% (4/6)
      · −4.0% : fill 2% (2/66) · rebond 71% (1/2)
      · −5.0% : fill 0% (1/66) · rebond 0% (0/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 76% si les 15 1res min sont vertes (61 cas) · 23% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **54min** → P(séance verte=clôture>ouverture) 83% si début vert vs 13% si rouge (base 45% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 195min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=65) : tient le vert **83%** · continue >prix actuel 60% ; creux résiduel méd -1.34% (q20 -2.99%) → **SL/trailing à −2.99%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.54% / q75 +2.67% → **scale +1.54% / runner +2.67%**, sortie à la clôture
  - **si ROUGE au coude** (n=95) : edge inversé — récupère vert seulement **13%** (continue à baisser 57%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.41%** (au-delà de la MAE q10 -3.41%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.66% .. +2.57%] · haut q95 +3.59% · bas q05 -3.91%
   - 60min (n=160) : retour [-3.0% .. +3.93%] · haut q95 +4.6% · bas q05 -4.11%
   - 2h (n=160) : retour [-3.39% .. +4.07%] · haut q95 +5.13% · bas q05 -4.21%
   - 4h (n=160) : retour [-3.57% .. +6.33%] · haut q95 +7.05% · bas q05 -5.12%
   - 6h (n=160) : retour [-4.46% .. +5.17%] · haut q95 +7.94% · bas q05 -5.55%
   - session (n=160) : retour [-4.52% .. +5.15%] · haut q95 +7.94% · bas q05 -5.55%


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
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.8  _(neutre)_
- **ADX** : 15.0  _(pas de tendance nette)_
- **MACD** : hist -74.904  _(bearish_recent)_
- **BB** : %B 0.43 · largeur 9.7%
- **ATR** : 4014.29 (41.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.115  _(accumulation)_
- **Vol ratio** : 0.81  _(volume normal)_
- **Choppiness** : 55.8  _(transition)_
- **MA** : MA20 86965.0 · MA50 83700.0 · MA200 103349.5  _(prix < MA20)_
- **Dist MA** : MA20 -0.6% · MA50 +3.2% · MA200 -16.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (477610 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
