# 207940

**Generated** : 2026-09-01T21:57:19.459108+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1520000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1520000.00 (+4.2% vs entrée) · entrée ₩1458125.00 · stop ₩1341475.00 · T1 ₩1477408.90 · R/R 0.17  
> ↳ P(T1 av. stop) 57 % · EV/risk -0.021 · ¼-Kelly 0.102 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1454268.22–₩1461981.78 (mid ₩1458125.00)
- Spot actuel : ₩1520000.00 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1341475.00 (stop swing_plan-based (-12.46%))
- Targets : T1 ₩1477408.90 · R/R 0.17 | T2 ₩1496692.81 · R/R 0.33 | T3 ₩1515976.71 · R/R 0.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1341475.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (12.46 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.46 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.282 % | p01 -2.672 % | pire -5.458 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0048** [0.0004 ; 0.0249] _(largeur 2.4 pt, n_eff 173.1)_
   - swing : **0.3353** [0.2871 ; 0.3863] _(largeur 9.9 pt, n_eff 345.6)_
   - deep : **0.335** [0.2868 ; 0.386] _(largeur 9.9 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.54 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.59 % contre 2.80 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.62 % vs -6.24 % si l'on extrapolait par √5 _(rapport 0.9 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3213** (β de hausse 0.2172, asymétrie 1.4793) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : ₩-2427.561 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 34 % | T3 10 %
- Kelly (position) : f* 0.406 | ¼-Kelly 0.102 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 39.3 | bear 54.8 | side 5.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=13, n_eff=8))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→66% · +2.0%→45% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.12% (p90 6.65%) · excursion haute méd. +1.52% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.725% vs midi 0.75% vs clôture 0.917% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑1%/↓2% ; spike-down 53% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.068)_ ; drift intra méd. 0.091% ; recovery-V 37%
- **σ réalisé intraday** 2.64% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 37% / whipsaw 11%
- POC intraday (dernière séance, temps-au-prix) : 1507400.0 (VA 1481800.0–1510600.0 ; dernier close 1513000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 71% · **stop −2.99%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.55 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 40% (gap-down >1% 12% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.87% (p90 −2.31%) · haut méd +0.51% · range méd 1.46%
- Excursion ouverture 15min (n=160) : bas méd −1.1% (p90 −2.93%) · haut méd +0.63% · range méd 1.93%
- Excursion ouverture 30min (n=160) : bas méd −1.23% (p90 −3.25%) · haut méd +0.74% · range méd 2.19%
- Excursion ouverture 60min (n=160) : bas méd −1.27% (p90 −3.5%) · haut méd +0.92% · range méd 2.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1518000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (111/159) · gap 24% · délai 0.3min · rebond 61% (56/111) (MFE +1.27%)
   - −1.0% : fill 30min 52% · séance 63% (89/159) · gap 12% · délai 1.2min · rebond 60% (44/89) (MFE +1.55%)
   - −1.5% : fill 30min 43% · séance 53% (73/159) · gap 8% · délai 2.5min · rebond 61% (37/73) (MFE +1.54%)
   - −2.0% : fill 30min 30% · séance 44% (60/159) · gap 6% · délai 4.8min · rebond 71% (35/60) (MFE +1.64%)
   - −3.0% : fill 30min 12% · séance 24% (36/159) · gap 3% · délai 28.1min · rebond 51% (18/36) (MFE +1.03%)
   - −4.0% : fill 30min 7% · séance 15% (20/159) · gap 3% · délai 52.1min · rebond 56% (11/20) (MFE +1.35%)
   - −5.0% : fill 30min 3% · séance 8% (11/159) · gap 3% · délai 116.7min · rebond 79% (8/11) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.84% (p90 −2.17%) → stop au-delà de −1.54% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −2.14%) → stop au-delà de −1.72% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=410 jambes) : jambe baissière méd −1.07% (p90 −2.65%) · ~7.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 100% (41/42) · rebond 65% (22/41)
      · −2.0% : fill 82% (33/42) · rebond 76% (19/33)
      · −3.0% : fill 34% (18/42) · rebond 44% (9/18)
      · −4.0% : fill 24% (10/42) · rebond 59% (5/10)
      · −5.0% : fill 14% (6/42) · rebond 100% (6/6)
   - **flat** (49 séances) :
      · −1.0% : fill 64% (29/49) · rebond 40% (10/29)
      · −2.0% : fill 35% (14/49) · rebond 42% (6/14)
      · −3.0% : fill 31% (10/49) · rebond 60% (6/10)
      · −4.0% : fill 17% (6/49) · rebond 62% (4/6)
      · −5.0% : fill 7% (3/49) · rebond 52% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 33% (19/68) · rebond 75% (12/19)
      · −2.0% : fill 20% (13/68) · rebond 89% (10/13)
      · −3.0% : fill 12% (8/68) · rebond 53% (3/8)
      · −4.0% : fill 7% (4/68) · rebond 42% (2/4)
      · −5.0% : fill 4% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 67% si les 15 1res min sont vertes (54 cas) · 32% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 74% si début vert vs 27% si rouge (base 45% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **74%** · continue >prix actuel 44% ; creux résiduel méd -1.54% (q20 -2.22%) → **SL/trailing à −2.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.27% → **scale +1.29% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **27%** (continue à baisser 50%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.58%** (au-delà de la MAE q10 -3.58%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.29% .. +3.11%] · haut q95 +3.33% · bas q05 -3.65%
   - 60min (n=160) : retour [-3.55% .. +2.65%] · haut q95 +3.5% · bas q05 -4.21%
   - 2h (n=160) : retour [-3.66% .. +3.35%] · haut q95 +4.3% · bas q05 -4.68%
   - 4h (n=160) : retour [-4.52% .. +2.98%] · haut q95 +4.82% · bas q05 -5.38%
   - 6h (n=160) : retour [-4.72% .. +3.64%] · haut q95 +4.82% · bas q05 -5.47%
   - session (n=160) : retour [-4.41% .. +3.28%] · haut q95 +4.82% · bas q05 -5.57%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.04%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 37.9  _(momentum baissier)_
- **ADX** : 16.1  _(pas de tendance nette)_
- **MACD** : hist -10754.22  _(bearish_recent)_
- **BB** : %B 0.32 · largeur 9.8%
- **ATR** : 53285.71 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.261  _(accumulation)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 50.5  _(transition)_
- **MA** : MA20 1547550.0 · MA50 1463380.0 · MA200 1586683.23  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 +3.9% · MA200 -4.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (498144 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
