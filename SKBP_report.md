# 326030

**Generated** : 2026-08-24T21:57:47.488432+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩86100.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩86100.00 (+1.3% vs entrée) · entrée ₩84983.33 · stop ₩83708.58 · T1 ₩86136.42 · R/R 0.9  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.011 _(réel 5 s)_ (GBM -0.001) · ¼-Kelly 0.01 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 122 % hors [0,100] (R² max 0.65). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩84752.72–₩85213.95 (mid ₩84983.33)
- Spot actuel : ₩86100.00 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : ₩83708.58 (stop swing_plan-based (-7.08%))
- Targets : T1 ₩86136.42 · R/R 0.9 | T2 ₩87289.50 · R/R 1.81 | T3 ₩88442.59 · R/R 2.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩83708.58


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.98 % < 1 % et 83 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (7.08 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 7.08 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.59 % | p01 -2.833 % | pire -5.539 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0748** [0.0425 ; 0.1211] _(largeur 7.9 pt, n_eff 173.1)_
   - swing : **0.3896** [0.3393 ; 0.4418] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.5241** [0.4714 ; 0.5764] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.5 pt), swing (40.3 pt), deep (32.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.53 %** | CVaR **-6.33 %** | vol 2.86 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 1.81 % contre 3.49 % aujourd'hui, rapport 0.52)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.37 % vs -8.48 % si l'on extrapolait par √5 _(rapport 0.987 ; < 1 = le √5 surestime)_
- **β de baisse : 0.6117** (β de hausse 0.4546, asymétrie 1.3456) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.001 | EV/share : ₩-1.242 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 54 % | T2 35 % | T3 16 %
- Kelly (position) : f* 0.041 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.2 | bear 19.2 | side 74.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.299% → cible +1.357% / stop −1.5%, p_fill 69%, n_eff≈26.2) : P(cible|rempli) **48%** · **EV/risk -0.011** (×p_fill ; si rempli -0.02% du capital)
  - **swing** (entrée dip −2.858% → cible +3.034% / stop −4.347%, p_fill 49%, n_eff≈21.1) : P(cible|rempli) **48%** · **EV/risk -0.096** (×p_fill ; si rempli -0.85% du capital)
  - **deep** (entrée dip −4.406% → cible +4.291% / stop −6.626%, p_fill 47%, n_eff≈25.3) : P(cible|rempli) **75%** · **EV/risk +0.110** (×p_fill ; si rempli +1.55% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 66.1  _(momentum haussier)_
- **ADX** : 15.5  _(pas de tendance nette)_
- **MACD** : hist 212.01  _(pas de croisement recent)_
- **BB** : %B 0.65 · largeur 20.0%
- **ATR** : 3635.71 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.105  _(accumulation)_
- **Vol ratio** : 0.5  _(volume atone)_
- **Choppiness** : 46.3  _(transition)_
- **MA** : MA20 83590.0 · MA50 83686.0 · MA200 104560.5  _(prix > MA20)_
- **Dist MA** : MA20 +3.0% · MA50 +2.9% · MA200 -17.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (763816 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
