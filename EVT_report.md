# EVT

**Generated** : 2026-08-21T00:04:55.916600+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €3.34  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €3.34 (+1.2% vs entrée) · entrée €3.30 · stop €3.25 · T1 €3.35 · R/R 1.0  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.069 _(réel 5 s)_ (GBM -0.026) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −1.5% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €3.29–€3.31 (mid €3.30)
- Spot actuel : €3.34 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €3.25 (stop swing_plan-based (-7.43%))
- Targets : T1 €3.35 · R/R 1.0 | T2 €3.40 · R/R 2.0 | T3 €3.45 · R/R 3.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €3.25


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.36 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.43 %)** : le gap seul le franchit 0.393 % des séances (5 fois sur 1273).
   - exécution **6.394 pt plus bas** dans le cas TYPIQUE (médiane), 20.662 au p90, **24.983 au pire**
   - perte réelle **18.001 %** en moyenne _(tirée par la queue)_, jusqu'à **32.413 %** — au lieu des 7.43 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0415 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.044 % | p01 -3.985 % | pire -32.413 % _(sur 1273 séances)_
- **P(stop avant cible)** _(source : daily, 1274 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0671** [0.0368 ; 0.1117] _(largeur 7.5 pt, n_eff 173.1)_
   - swing : **0.4205** [0.3693 ; 0.473] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4924** [0.44 ; 0.545] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.1 pt), swing (45.2 pt), deep (43.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1200 séances)** : VaR **-5.11 %** | CVaR **-9.26 %** | vol 3.81 %/j
   - _fenêtre arrêtée : rupture de regime a 1260 seances en arriere (volatilite 2.11 % contre 4.00 % aujourd'hui, rapport 0.53)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.97 % vs -11.13 % si l'on extrapolait par √5 _(rapport 1.165 ; < 1 = le √5 surestime)_
- **β de baisse : 1.1133** (β de hausse 0.942, asymétrie 1.1819) vs GDAXI — 600 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.026 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 20 % | T3 6 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 76.4 | bear 8.0 | side 15.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.217% → cible +1.553% / stop −1.501%, p_fill 69%, n_eff≈26.9) : P(cible|rempli) **50%** · **EV/risk +0.069** (×p_fill ; si rempli +0.15% du capital)
  - **swing** (entrée dip −2.667% → cible +3.472% / stop −4.894%, p_fill 40%, n_eff≈16.3) : P(cible|rempli) **51%** · **EV/risk -0.041** (×p_fill ; si rempli -0.51% du capital)
  - **deep** (entrée dip −4.125% → cible +4.909% / stop −7.452%, p_fill 32%, n_eff≈17.9) : P(cible|rempli) **30%** · **EV/risk -0.116** (×p_fill ; si rempli -2.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→46% · +3.0%→24% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.9% (p90 6.57%) · excursion haute méd. +1.82% / basse méd. −1.78%
- Profil de vol intra : ouverture 2.717% vs midi 1.234% vs clôture 1.204% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 94% · range 6% · trend ↑0%/↓0% ; spike-down 56% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.089 ; mean-reverting — autocorr -0.121)_ ; drift intra méd. -0.657% ; recovery-V 31%
- **σ réalisé intraday** 3.197% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 68% / bas 69% / whipsaw 39%
- POC intraday (dernière séance, temps-au-prix) : 3.2923 (VA 3.2668–3.3142 ; dernier close 3.364)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.0%** sous le close veille · fill 69% · rebond 72% · **stop −3.18%** sous le fill (sous le bruit) · cible +1.78% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 39% (gap-down >1% 16% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.48%) · haut méd +0.53% · range méd 1.47%
- Excursion ouverture 15min (n=160) : bas méd −0.85% (p90 −2.84%) · haut méd +0.79% · range méd 1.79%
- Excursion ouverture 30min (n=160) : bas méd −1.05% (p90 −2.85%) · haut méd +0.93% · range méd 2.21%
- Excursion ouverture 60min (n=160) : bas méd −1.11% (p90 −3.3%) · haut méd +0.97% · range méd 2.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 3.364 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 82% (133/159) · gap 23% · délai 0.3min · rebond 72% (89/133) (MFE +1.65%)
   - −1.0% : fill 30min 49% · séance 69% (116/159) · gap 16% · délai 1.8min · rebond 72% (75/116) (MFE +1.78%)
   - −1.5% : fill 30min 37% · séance 56% (96/159) · gap 12% · délai 7.8min · rebond 66% (61/96) (MFE +1.8%)
   - −2.0% : fill 30min 23% · séance 44% (80/159) · gap 7% · délai 23.5min · rebond 58% (50/80) (MFE +1.32%)
   - −3.0% : fill 30min 12% · séance 27% (55/159) · gap 4% · délai 51.4min · rebond 66% (40/55) (MFE +1.36%)
   - −4.0% : fill 30min 6% · séance 17% (32/159) · gap 2% · délai 53.0min · rebond 60% (20/32) (MFE +1.67%)
   - −5.0% : fill 30min 4% · séance 9% (18/159) · gap 1% · délai 56.0min · rebond 60% (12/18) (MFE +1.82%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.49%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.36% (p90 −1.71%) → stop au-delà de −1.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.31% (p90 −1.89%) → stop au-delà de −1.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=817 jambes) : jambe baissière méd −1.07% (p90 −2.32%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (58 séances) :
      · −1.0% : fill 95% (55/58) · rebond 71% (32/55)
      · −2.0% : fill 64% (41/58) · rebond 60% (25/41)
      · −3.0% : fill 38% (29/58) · rebond 68% (21/29)
      · −4.0% : fill 27% (20/58) · rebond 56% (14/20)
      · −5.0% : fill 16% (13/58) · rebond 57% (9/13)
   - **flat** (43 séances) :
      · −1.0% : fill 65% (30/43) · rebond 73% (23/30)
      · −2.0% : fill 48% (20/43) · rebond 64% (13/20)
      · −3.0% : fill 34% (13/43) · rebond 77% (10/13)
      · −4.0% : fill 17% (6/43) · rebond 46% (2/6)
      · −5.0% : fill 6% (3/43) · rebond 27% (1/3)
   - **gap-up** (58 séances) :
      · −1.0% : fill 54% (31/58) · rebond 72% (20/31)
      · −2.0% : fill 26% (19/58) · rebond 46% (12/19)
      · −3.0% : fill 14% (13/58) · rebond 40% (9/13)
      · −4.0% : fill 9% (6/58) · rebond 90% (4/6)
      · −5.0% : fill 5% (2/58) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 64% si les 15 1res min sont vertes (72 cas) · 38% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **5min** → P(séance verte=clôture>ouverture) 66% si début vert vs 38% si rouge (base 50% · écart 29 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=69) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.75% (q20 -2.4%) → **SL/trailing à −2.4%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.43% → **scale +1.55% / runner +2.43%**, sortie à la clôture
  - **si ROUGE au coude** (n=91) : edge inversé — récupère vert seulement **38%** (continue à baisser 50%) → **RÉDUIRE ~63%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.73%** (au-delà de la MAE q10 -4.73%), cible rebond +1.77% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.65% .. +2.31%] · haut q95 +3.38% · bas q05 -3.94%
   - 60min (n=160) : retour [-3.97% .. +2.7%] · haut q95 +3.49% · bas q05 -4.88%
   - 2h (n=160) : retour [-4.35% .. +2.71%] · haut q95 +3.94% · bas q05 -5.29%
   - 4h (n=160) : retour [-3.51% .. +3.19%] · haut q95 +3.94% · bas q05 -6.67%
   - 6h (n=160) : retour [-3.77% .. +3.46%] · haut q95 +5.05% · bas q05 -6.67%
   - session (n=160) : retour [-4.61% .. +4.31%] · haut q95 +6.59% · bas q05 -7.56%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — EVT = **volatil sans tendance propre (choppy)** (vol intra méd 2.95%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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

- **RSI** : 45.2  _(neutre)_
- **ADX** : 31.4  _(tendance etablie)_
- **MACD** : hist 0.027  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 14.2%
- **ATR** : 0.16 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.332  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 3.49 · MA50 4.13 · MA200 5.07  _(prix < MA20)_
- **Dist MA** : MA20 -4.3% · MA50 -19.2% · MA200 -34.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (576514 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
