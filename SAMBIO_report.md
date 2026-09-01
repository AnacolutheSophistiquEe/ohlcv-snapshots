# 207940

**Generated** : 2026-09-01T00:20:55.376010+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1507000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1507000.00 (+9.4% vs entrée) · entrée ₩1378025.00 · stop ₩1323025.00 · T1 ₩1421912.59 · R/R 0.8  
> ↳ P(T1 av. stop) 44 % · EV/risk -0.077 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1369247.48–₩1386802.52 (mid ₩1378025.00)
- Spot actuel : ₩1507000.00 (+9.4% au-dessus de la zone — repli à attendre)
- Stop : ₩1323025.00 (stop swing_plan-based (-12.21%))
- Targets : T1 ₩1421912.59 · R/R 0.8 | T2 ₩1465800.18 · R/R 1.6 | T3 ₩1509687.77 · R/R 2.39
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1323025.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (12.21 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 12.21 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.283 % | p01 -2.673 % | pire -5.458 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0049** [0.0004 ; 0.025] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.3343** [0.2861 ; 0.3853] _(largeur 9.9 pt, n_eff 345.6)_
   - deep : **0.3214** [0.2738 ; 0.372] _(largeur 9.8 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.54 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.58 % contre 2.82 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.62 % vs -6.25 % si l'on extrapolait par √5 _(rapport 0.9 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3213** (β de hausse 0.2181, asymétrie 1.473) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.077 | EV/share : ₩-4257.366 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 23 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 24.1 | bear 70.1 | side 5.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=14, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→66% · +2.0%→44% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.11% (p90 6.65%) · excursion haute méd. +1.47% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.712% vs midi 0.751% vs clôture 0.915% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 11% · trend ↑1%/↓2% ; spike-down 52% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.059)_ ; drift intra méd. -0.009% ; recovery-V 33%
- **σ réalisé intraday** 2.643% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 39% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1507287.5 (VA 1489587.5–1520562.5 ; dernier close 1486000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 43% · rebond 70% · **stop −3.05%** sous le fill (sous le bruit) · cible +1.55% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 39% (gap-down >1% 12% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.86% (p90 −2.33%) · haut méd +0.51% · range méd 1.46%
- Excursion ouverture 15min (n=160) : bas méd −1.08% (p90 −2.93%) · haut méd +0.65% · range méd 1.91%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.32%) · haut méd +0.84% · range méd 2.12%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.52%) · haut méd +0.94% · range méd 2.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1486000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 78% (111/159) · gap 24% · délai 0.4min · rebond 60% (55/111) (MFE +1.24%)
   - −1.0% : fill 30min 52% · séance 62% (89/159) · gap 12% · délai 1.3min · rebond 59% (43/89) (MFE +1.47%)
   - −1.5% : fill 30min 42% · séance 52% (73/159) · gap 8% · délai 2.3min · rebond 60% (37/73) (MFE +1.46%)
   - −2.0% : fill 30min 29% · séance 43% (60/159) · gap 7% · délai 5.0min · rebond 70% (35/60) (MFE +1.55%)
   - −3.0% : fill 30min 13% · séance 25% (36/159) · gap 3% · délai 28.1min · rebond 51% (18/36) (MFE +1.03%)
   - −4.0% : fill 30min 7% · séance 15% (20/159) · gap 3% · délai 52.1min · rebond 56% (11/20) (MFE +1.35%)
   - −5.0% : fill 30min 3% · séance 8% (11/159) · gap 3% · délai 116.7min · rebond 79% (8/11) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.79% (p90 −2.05%) → stop au-delà de −1.43% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −2.0%) → stop au-delà de −1.56% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=409 jambes) : jambe baissière méd −1.07% (p90 −2.67%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 100% (41/42) · rebond 63% (21/41)
      · −2.0% : fill 80% (33/42) · rebond 75% (19/33)
      · −3.0% : fill 36% (18/42) · rebond 44% (9/18)
      · −4.0% : fill 26% (10/42) · rebond 59% (5/10)
      · −5.0% : fill 15% (6/42) · rebond 100% (6/6)
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
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 67% si les 15 1res min sont vertes (54 cas) · 30% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 74% si début vert vs 24% si rouge (base 44% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=57) : tient le vert **74%** · continue >prix actuel 44% ; creux résiduel méd -1.54% (q20 -2.22%) → **SL/trailing à −2.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.27% → **scale +1.29% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=103) : edge inversé — récupère vert seulement **24%** (continue à baisser 51%) → **RÉDUIRE ~76%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.61%** (au-delà de la MAE q10 -3.61%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.29% .. +3.12%] · haut q95 +3.37% · bas q05 -3.73%
   - 60min (n=160) : retour [-3.55% .. +2.69%] · haut q95 +3.56% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.69% .. +3.36%] · haut q95 +4.33% · bas q05 -4.68%
   - 4h (n=160) : retour [-4.69% .. +3.04%] · haut q95 +4.83% · bas q05 -5.38%
   - 6h (n=160) : retour [-4.72% .. +3.68%] · haut q95 +4.83% · bas q05 -5.56%
   - session (n=160) : retour [-4.45% .. +3.32%] · haut q95 +4.83% · bas q05 -5.64%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.04%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 42.2  _(momentum baissier)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist -10226.222  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 12.2%
- **ATR** : 55000.0 (55.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.148  _(accumulation)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 1542150.0 · MA50 1460240.0 · MA200 1588414.88  _(prix < MA20)_
- **Dist MA** : MA20 -2.3% · MA50 +3.2% · MA200 -5.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (502365 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
