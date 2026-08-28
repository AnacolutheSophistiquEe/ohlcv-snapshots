# 207940

**Generated** : 2026-08-28T21:57:26.048927+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1481000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1481000.00 (+8.4% vs entrée) · entrée ₩1366325.00 · stop ₩1312825.00 · T1 ₩1411553.16 · R/R 0.85  
> ↳ P(T1 av. stop) 42 % · EV/risk -0.077 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1357279.37–₩1375370.63 (mid ₩1366325.00)
- Spot actuel : ₩1481000.00 (+8.4% au-dessus de la zone — repli à attendre)
- Stop : ₩1312825.00 (stop swing_plan-based (-11.36%))
- Targets : T1 ₩1411553.16 · R/R 0.85 | T2 ₩1456781.31 · R/R 1.69 | T3 ₩1502009.47 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1312825.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (11.36 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.36 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.282 % | p01 -2.672 % | pire -5.458 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0049** [0.0004 ; 0.025] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.3555** [0.3064 ; 0.407] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3487** [0.2999 ; 0.4] _(largeur 10.0 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 9.4 observations effectives », dont la borne haute a 95 % vaut environ 31.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (56.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.89 %** | vol 2.54 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.59 % contre 2.82 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.62 % vs -6.24 % si l'on extrapolait par √5 _(rapport 0.9 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3183** (β de hausse 0.2192, asymétrie 1.4523) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.077 | EV/share : ₩-4138.167 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 21 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 17.8 | bear 77.0 | side 5.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.522% → cible +1.48% / stop −8.0%, p_fill 19%, n_eff≈9.4) : P(cible|rempli) **50%** · **EV/risk +0.006** (×p_fill ; si rempli +0.27% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→65% · +2.0%→42% · +3.0%→26% · +5.0%→6% · +8.0%→2%
- Range intraday médian 4.11% (p90 6.65%) · excursion haute méd. +1.39% / basse méd. −1.96%
- Profil de vol intra : ouverture 2.698% vs midi 0.749% vs clôture 0.912% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 11% · trend ↑1%/↓2% ; spike-down 51% · recovery-V 34%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. 0.057% ; recovery-V 35%
- **σ réalisé intraday** 2.658% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 41% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1588887.5 (VA 1587162.5–1594062.5 ; dernier close 1592000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 42% · rebond 73% · **stop −2.79%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.59 (high win-rate)
- Gaps overnight (n=159) : méd. 0.07% · baisse 38% (gap-down >1% 11% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.86% (p90 −2.35%) · haut méd +0.52% · range méd 1.44%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.93%) · haut méd +0.66% · range méd 1.88%
- Excursion ouverture 30min (n=160) : bas méd −1.15% (p90 −3.35%) · haut méd +0.86% · range méd 2.24%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.53%) · haut méd +0.92% · range méd 2.46%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1594000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 78% (111/159) · gap 23% · délai 0.4min · rebond 62% (55/111) (MFE +1.27%)
   - −1.0% : fill 30min 51% · séance 61% (89/159) · gap 11% · délai 1.4min · rebond 61% (43/89) (MFE +1.54%)
   - −1.5% : fill 30min 41% · séance 51% (73/159) · gap 7% · délai 2.5min · rebond 62% (38/73) (MFE +1.52%)
   - −2.0% : fill 30min 27% · séance 42% (60/159) · gap 5% · délai 5.7min · rebond 73% (36/60) (MFE +1.64%)
   - −3.0% : fill 30min 11% · séance 24% (36/159) · gap 1% · délai 32.6min · rebond 56% (19/36) (MFE +1.17%)
   - −4.0% : fill 30min 6% · séance 14% (19/159) · gap 1% · délai 65.7min · rebond 64% (11/19) (MFE +1.52%)
   - −5.0% : fill 30min 1% · séance 6% (10/159) · gap 1% · délai 173.8min · rebond 72% (7/10) (MFE +1.59%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.77% (p90 −2.06%) → stop au-delà de −1.36% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.9% (p90 −2.04%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=408 jambes) : jambe baissière méd −1.07% (p90 −2.69%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 99% (40/41) · rebond 67% (21/40)
      · −2.0% : fill 79% (32/41) · rebond 81% (19/32)
      · −3.0% : fill 32% (17/41) · rebond 53% (9/17)
      · −4.0% : fill 21% (9/41) · rebond 76% (5/9)
      · −5.0% : fill 9% (5/41) · rebond 100% (5/5)
   - **flat** (49 séances) :
      · −1.0% : fill 64% (29/49) · rebond 40% (10/29)
      · −2.0% : fill 35% (14/49) · rebond 42% (6/14)
      · −3.0% : fill 31% (10/49) · rebond 60% (6/10)
      · −4.0% : fill 17% (6/49) · rebond 62% (4/6)
      · −5.0% : fill 7% (3/49) · rebond 52% (1/3)
   - **gap-up** (69 séances) :
      · −1.0% : fill 33% (20/69) · rebond 74% (12/20)
      · −2.0% : fill 21% (14/69) · rebond 89% (11/14)
      · −3.0% : fill 13% (9/69) · rebond 54% (4/9)
      · −4.0% : fill 7% (4/69) · rebond 42% (2/4)
      · −5.0% : fill 4% (2/69) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 68% si les 15 1res min sont vertes (55 cas) · 31% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 74% si début vert vs 25% si rouge (base 45% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 225min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=58) : tient le vert **74%** · continue >prix actuel 44% ; creux résiduel méd -1.53% (q20 -2.22%) → **SL/trailing à −2.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.29% / q75 +2.27% → **scale +1.29% / runner +2.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=102) : edge inversé — récupère vert seulement **25%** (continue à baisser 50%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.64%** (au-delà de la MAE q10 -3.64%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.3% .. +3.14%] · haut q95 +3.42% · bas q05 -3.82%
   - 60min (n=160) : retour [-3.55% .. +2.71%] · haut q95 +3.61% · bas q05 -4.23%
   - 2h (n=160) : retour [-3.72% .. +3.37%] · haut q95 +4.35% · bas q05 -4.68%
   - 4h (n=160) : retour [-4.85% .. +3.12%] · haut q95 +4.86% · bas q05 -5.38%
   - 6h (n=160) : retour [-4.72% .. +3.72%] · haut q95 +4.86% · bas q05 -5.65%
   - session (n=160) : retour [-4.48% .. +3.36%] · haut q95 +4.86% · bas q05 -5.72%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.04%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -7364.54  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 12.6%
- **ATR** : 53500.0 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.096  _(accumulation)_
- **Vol ratio** : 1.77  _(volume au-dessus de la moyenne)_
- **Choppiness** : 57.3  _(transition)_
- **MA** : MA20 1540800.0 · MA50 1458600.0 · MA200 1590241.54  _(prix < MA20)_
- **Dist MA** : MA20 -3.9% · MA50 +1.5% · MA200 -6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (616215 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
