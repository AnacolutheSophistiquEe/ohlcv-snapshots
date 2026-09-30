# 207940

**Generated** : 2026-09-30T00:23:06.666927+00:00  
**Santé technique** : 5/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩1385000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1385000.00 (+2.1% vs entrée) · entrée ₩1356875.00 · stop ₩1343306.25 · T1 ₩1366682.76 · R/R 0.72  
> ↳ _probas brutes, non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1354913.45–₩1358836.55 (mid ₩1356875.00)
- Spot actuel : ₩1385000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩1343306.25 (plancher anti-bruit (R/R<2) ; -1.00 % depuis l'entree)
- Targets : T1 ₩1366682.76 · R/R 0.72 | T2 ₩1376490.51 · R/R 1.45 | T3 ₩1386298.27 · R/R 2.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1343306.25


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (6.72 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 6.72 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.276 % | p01 -2.672 % | pire -5.458 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5026** [0.4286 ; 0.5765] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4526** [0.4007 ; 0.5053] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.4154** [0.3643 ; 0.4679] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (27.6 pt), swing (31.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.56 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.54 % contre 2.66 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.55 % vs -6.16 % si l'on extrapolait par √5 _(rapport 0.901 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3122** (β de hausse 0.2187, asymétrie 1.4276) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 74.8 | side 20.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.03% → cible +0.723% / stop −1.0%, p_fill 44%, n_eff≈47.9) : P(cible|rempli) **52%** · **EV/risk -0.044** (×p_fill ; si rempli -0.10% du capital)
  - **swing** (entrée dip −4.472% → cible +1.616% / stop −2.354%, p_fill 24%, n_eff≈27.2) : P(cible|rempli) **74%** · **EV/risk +0.054** (×p_fill ; si rempli +0.53% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=14, n_eff=14))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→55% · +2.0%→35% · +3.0%→23% · +5.0%→4% · +8.0%→2%
- Range intraday médian 3.8% (p90 6.09%) · excursion haute méd. +1.08% / basse méd. −1.59%
- Profil de vol intra : ouverture 2.295% vs midi 0.651% vs clôture 0.791% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 14% · trend ↑1%/↓2% ; spike-down 53% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; mean-reverting — autocorr -0.067)_ ; drift intra méd. -0.131% ; recovery-V 31%
- **σ réalisé intraday** 2.411% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 58% / bas 40% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 1441612.5 (VA 1433662.5–1454862.5 ; dernier close 1446000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 44% · rebond 62% · **stop −2.98%** sous le fill (sous le bruit) · cible +1.39% · R/R 0.47 (high win-rate)
- Gaps overnight (n=153) : méd. 0.07% · baisse 39% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −0.78% (p90 −2.25%) · haut méd +0.5% · range méd 1.38%
- Excursion ouverture 15min (n=160) : bas méd −1.03% (p90 −2.87%) · haut méd +0.6% · range méd 1.82%
- Excursion ouverture 30min (n=160) : bas méd −1.08% (p90 −3.15%) · haut méd +0.8% · range méd 2.06%
- Excursion ouverture 60min (n=160) : bas méd −1.26% (p90 −3.5%) · haut méd +0.92% · range méd 2.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1447000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 79% (106/153) · gap 24% · délai 0.2min · rebond 56% (50/106) (MFE +1.16%)
   - −1.0% : fill 30min 50% · séance 64% (87/153) · gap 16% · délai 1.3min · rebond 57% (41/87) (MFE +1.28%)
   - −1.5% : fill 30min 39% · séance 53% (70/153) · gap 10% · délai 2.4min · rebond 55% (33/70) (MFE +1.44%)
   - −2.0% : fill 30min 27% · séance 44% (59/153) · gap 6% · délai 4.8min · rebond 62% (32/59) (MFE +1.39%)
   - −3.0% : fill 30min 12% · séance 25% (36/153) · gap 3% · délai 29.9min · rebond 46% (18/36) (MFE +0.92%)
   - −4.0% : fill 30min 7% · séance 15% (19/153) · gap 3% · délai 47.5min · rebond 56% (10/19) (MFE +1.36%)
   - −5.0% : fill 30min 3% · séance 8% (11/153) · gap 3% · délai 116.1min · rebond 78% (8/11) (MFE +1.68%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.58% (p90 −2.08%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.93% (p90 −2.15%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.88% (p90 −2.12%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=408 jambes) : jambe baissière méd −1.07% (p90 −2.72%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (41 séances) :
      · −1.0% : fill 99% (40/41) · rebond 65% (21/40)
      · −2.0% : fill 72% (31/41) · rebond 73% (17/31)
      · −3.0% : fill 34% (18/41) · rebond 44% (9/18)
      · −4.0% : fill 24% (10/41) · rebond 58% (5/10)
      · −5.0% : fill 14% (6/41) · rebond 100% (6/6)
   - **flat** (44 séances) :
      · −1.0% : fill 67% (28/44) · rebond 32% (8/28)
      · −2.0% : fill 42% (15/44) · rebond 35% (6/15)
      · −3.0% : fill 37% (11/44) · rebond 49% (6/11)
      · −4.0% : fill 16% (6/44) · rebond 62% (4/6)
      · −5.0% : fill 7% (3/44) · rebond 51% (1/3)
   - **gap-up** (68 séances) :
      · −1.0% : fill 34% (19/68) · rebond 70% (12/19)
      · −2.0% : fill 22% (13/68) · rebond 68% (9/13)
      · −3.0% : fill 10% (7/68) · rebond 44% (3/7)
      · −4.0% : fill 6% (3/68) · rebond 38% (1/3)
      · −5.0% : fill 4% (2/68) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 70% si les 15 1res min sont vertes (55 cas) · 29% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 76% si début vert vs 23% si rouge (base 44% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 218min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **76%** · continue >prix actuel 41% ; creux résiduel méd -1.27% (q20 -1.9%) → **SL/trailing à −1.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.26% / q75 +2.23% → **scale +1.26% / runner +2.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **23%** (continue à baisser 55%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.56%** (au-delà de la MAE q10 -3.56%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.24% .. +2.74%] · haut q95 +3.23% · bas q05 -3.6%
   - 60min (n=160) : retour [-3.54% .. +2.52%] · haut q95 +3.37% · bas q05 -4.2%
   - 2h (n=160) : retour [-3.57% .. +3.3%] · haut q95 +4.23% · bas q05 -4.67%
   - 4h (n=160) : retour [-4.39% .. +2.87%] · haut q95 +4.82% · bas q05 -5.37%
   - 6h (n=160) : retour [-4.71% .. +3.52%] · haut q95 +4.82% · bas q05 -5.39%
   - session (n=160) : retour [-4.34% .. +3.25%] · haut q95 +4.82% · bas q05 -5.43%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 2.06%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.2 · part idiosyncratique 0.8
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.2  _(survente)_
- **ADX** : 24.9  _(pas de tendance nette)_
- **MACD** : hist -4123.709  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 12.5%
- **ATR** : 31142.86 (8.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.133  _(accumulation)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 49.2  _(transition)_
- **MA** : MA20 1431900.0 · MA50 1479280.0 · MA200 1553315.0  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 -6.4% · MA200 -10.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (551233 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
