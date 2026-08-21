# 207940

**Generated** : 2026-08-21T21:57:04.822621+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1551000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1551000.00 (+4.7% vs entrée) · entrée ₩1481375.00 · stop ₩1362865.00 · T1 ₩1559356.11 · R/R 0.66  
> ↳ P(T1 av. stop) 6 % · EV/risk -0.047 · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1476067.91–₩1486682.09 (mid ₩1481375.00)
- Spot actuel : ₩1551000.00 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1362865.00 (stop swing_plan-based (-13.45%))
- Targets : T1 ₩1559356.11 · R/R 0.66 | T2 ₩1560048.09 · R/R 0.66 | T3 ₩1560740.08 · R/R 0.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1362865.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.49 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (13.45 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.45 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.255 % | p01 -2.574 % | pire -5.373 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0678** [0.0373 ; 0.1125] _(largeur 7.5 pt, n_eff 173.1)_
   - swing : **0.2952** [0.249 ; 0.3448] _(largeur 9.6 pt, n_eff 345.6)_
   - deep : **0.4407** [0.389 ; 0.4934] _(largeur 10.4 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.95 %** | CVaR **-5.65 %** | vol 2.5 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 1.85 % contre 3.04 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.65 % vs -6.24 % si l'on extrapolait par √5 _(rapport 0.905 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3223** (β de hausse 0.218, asymétrie 1.478) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.047 | EV/share : ₩-5569.970 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 6 % | T3 6 %
- Kelly (position) : f* 0.062 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 72.7 | bear 20.0 | side 7.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=7))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→41% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.11% (p90 6.65%) · excursion haute méd. +1.27% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.669% vs midi 0.764% vs clôture 0.884% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (158 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 12% · trend ↑1%/↓2% ; spike-down 56% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -0.042% ; recovery-V 40%
- **σ réalisé intraday** 2.89% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 41% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 1586012.5 (VA 1569037.5–1598137.5 ; dernier close 1568000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 41% · rebond 67% · **stop −2.76%** sous le fill (sous le bruit) · cible +1.4% · R/R 0.51 (high win-rate)
- Gaps overnight (n=157) : méd. 0.3% · baisse 33% (gap-down >1% 10% · >2% 3%)
- Excursion ouverture 5min (n=158) : bas méd −0.86% (p90 −2.41%) · haut méd +0.51% · range méd 1.48%
- Excursion ouverture 15min (n=158) : bas méd −1.11% (p90 −3.0%) · haut méd +0.68% · range méd 1.96%
- Excursion ouverture 30min (n=158) : bas méd −1.25% (p90 −3.39%) · haut méd +0.84% · range méd 2.38%
- Excursion ouverture 60min (n=158) : bas méd −1.29% (p90 −3.6%) · haut méd +0.9% · range méd 2.53%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1568000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 76% (108/157) · gap 20% · délai 1.1min · rebond 57% (51/108) (MFE +1.15%)
   - −1.0% : fill 30min 46% · séance 60% (85/157) · gap 10% · délai 2.5min · rebond 57% (39/85) (MFE +1.3%)
   - −1.5% : fill 30min 37% · séance 48% (66/157) · gap 6% · délai 3.2min · rebond 54% (31/66) (MFE +1.42%)
   - −2.0% : fill 30min 28% · séance 41% (57/157) · gap 3% · délai 7.1min · rebond 67% (32/57) (MFE +1.4%)
   - −3.0% : fill 30min 10% · séance 25% (35/157) · gap 1% · délai 87.0min · rebond 57% (19/35) (MFE +1.39%)
   - −4.0% : fill 30min 3% · séance 14% (18/157) · gap 1% · délai 73.5min · rebond 68% (11/18) (MFE +1.74%)
   - −5.0% : fill 30min 1% · séance 7% (10/157) · gap 1% · délai 175.9min · rebond 72% (7/10) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.09%) → stop au-delà de −1.39% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.06%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=406 jambes) : jambe baissière méd −1.09% (p90 −2.76%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (37 séances) :
      · −1.0% : fill 99% (36/37) · rebond 66% (19/36)
      · −2.0% : fill 86% (31/37) · rebond 73% (17/31)
      · −3.0% : fill 37% (15/37) · rebond 54% (8/15)
      · −4.0% : fill 26% (9/37) · rebond 76% (5/9)
      · −5.0% : fill 12% (5/37) · rebond 100% (5/5)
   - **flat** (46 séances) :
      · −1.0% : fill 53% (24/46) · rebond 27% (7/24)
      · −2.0% : fill 33% (11/46) · rebond 45% (5/11)
      · −3.0% : fill 27% (8/46) · rebond 73% (6/8)
      · −4.0% : fill 12% (4/46) · rebond 100% (4/4)
      · −5.0% : fill 5% (2/46) · rebond 89% (1/2)
   - **gap-up** (74 séances) :
      · −1.0% : fill 43% (25/74) · rebond 64% (13/25)
      · −2.0% : fill 22% (15/74) · rebond 72% (10/15)
      · −3.0% : fill 18% (12/74) · rebond 49% (5/12)
      · −4.0% : fill 8% (5/74) · rebond 33% (2/5)
      · −5.0% : fill 5% (3/74) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=158) : 43% en base · 64% si les 15 1res min sont vertes (55 cas) · 31% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=158) : COUDE à **34min** → P(séance verte=clôture>ouverture) 74% si début vert vs 26% si rouge (base 43% · écart 48 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **74%** · continue >prix actuel 42% ; creux résiduel méd -1.77% (q20 -2.64%) → **SL/trailing à −2.64%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.36% / q75 +2.27% → **scale +1.36% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=102) : edge inversé — récupère vert seulement **26%** (continue à baisser 48%) → **RÉDUIRE ~74%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.68%** (au-delà de la MAE q10 -3.68%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=158) : retour [-3.34% .. +3.23%] · haut q95 +3.61% · bas q05 -4.04%
   - 60min (n=158) : retour [-3.58% .. +2.74%] · haut q95 +3.87% · bas q05 -4.25%
   - 2h (n=158) : retour [-3.87% .. +3.41%] · haut q95 +4.43% · bas q05 -4.7%
   - 4h (n=158) : retour [-4.89% .. +3.51%] · haut q95 +5.0% · bas q05 -5.47%
   - 6h (n=158) : retour [-4.73% .. +3.91%] · haut q95 +5.0% · bas q05 -6.08%
   - session (n=158) : retour [-4.59% .. +3.55%] · haut q95 +5.0% · bas q05 -6.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.07%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 57.8  _(momentum haussier)_
- **ADX** : 15.6  _(pas de tendance nette)_
- **MACD** : hist -1516.078  _(bearish_recent)_
- **BB** : %B 0.62 · largeur 11.1%
- **ATR** : 55428.57 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.261  _(accumulation)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 1530100.0 · MA50 1434280.0 · MA200 1598014.82  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 +8.1% · MA200 -2.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (602096 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
