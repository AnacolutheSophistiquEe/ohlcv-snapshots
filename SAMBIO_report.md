# 207940

**Generated** : 2026-10-01T21:59:53.640515+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · ₩1424956.50  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1424956.50 (+2.7% vs entrée) · entrée ₩1386842.38 · stop ₩1275894.99 · T1 ₩1403587.12 · R/R 0.15  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1384776.14–₩1388908.61 (mid ₩1386842.38)
- Spot actuel : ₩1424956.50 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : ₩1275894.99 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩1403587.12 · R/R 0.15 | T2 ₩1420331.86 · R/R 0.3 | T3 ₩1437076.60 · R/R 0.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1275894.99


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟢 **Régime de gap : gap_calme** — p_breach(-3 %)=0.57 % < 1 % et 100 % des franchissements viennent des 4 pires jours/an — la queue est TOUT, l'ordinaire est sans risque de gap
- **Au stop du plan (8.23 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 8.23 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.276 % | p01 -2.671 % | pire -5.458 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0038** [0.0003 ; 0.0229] _(largeur 2.3 pt, n_eff 173.1)_
   - swing : **0.5148** [0.4622 ; 0.5672] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5276** [0.4749 ; 0.5798] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 31.9 observations effectives », dont la borne haute a 95 % vaut environ 9.4 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.06 %** | CVaR **-5.87 %** | vol 2.56 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.53 % contre 2.66 % aujourd'hui, rapport 0.57)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -5.55 % vs -6.16 % si l'on extrapolait par √5 _(rapport 0.901 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3125** (β de hausse 0.2187, asymétrie 1.4286) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : ₩-4564.630 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 28 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 18.8 | side 76.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.674% → cible +1.207% / stop −8.0%, p_fill 25%, n_eff≈31.9) : P(cible|rempli) **48%** · **EV/risk +0.005** (×p_fill ; si rempli +0.17% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=12, n_eff=12))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→70% · +1.0%→53% · +2.0%→32% · +3.0%→20% · +5.0%→4% · +8.0%→2%
- Range intraday médian 3.63% (p90 6.09%) · excursion haute méd. +1.04% / basse méd. −1.54%
- Profil de vol intra : ouverture 2.247% vs midi 0.634% vs clôture 0.77% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 16% · trend ↑1%/↓1% ; spike-down 49% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.099)_ ; drift intra méd. -0.144% ; recovery-V 26%
- **σ réalisé intraday** 1.905% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 54% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 1397825.0 (VA 1392125.0–1400675.0 ; dernier close 1395000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 40% · rebond 60% · **stop −2.76%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.46 (high win-rate)
- Gaps overnight (n=152) : méd. 0.07% · baisse 40% (gap-down >1% 18% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.68% (p90 −2.07%) · haut méd +0.47% · range méd 1.27%
- Excursion ouverture 15min (n=160) : bas méd −0.88% (p90 −2.43%) · haut méd +0.56% · range méd 1.63%
- Excursion ouverture 30min (n=160) : bas méd −0.91% (p90 −2.61%) · haut méd +0.58% · range méd 1.73%
- Excursion ouverture 60min (n=160) : bas méd −1.07% (p90 −3.14%) · haut méd +0.75% · range méd 2.06%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1391000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 82% (111/152) · gap 26% · délai 0.3min · rebond 47% (51/111) (MFE +0.92%)
   - −1.0% : fill 30min 49% · séance 65% (90/152) · gap 18% · délai 1.2min · rebond 55% (44/90) (MFE +1.01%)
   - −1.5% : fill 30min 34% · séance 50% (71/152) · gap 8% · délai 2.7min · rebond 51% (32/71) (MFE +1.07%)
   - −2.0% : fill 30min 24% · séance 40% (58/152) · gap 5% · délai 6.2min · rebond 60% (31/58) (MFE +1.28%)
   - −3.0% : fill 30min 9% · séance 19% (34/152) · gap 2% · délai 29.9min · rebond 46% (17/34) (MFE +0.92%)
   - −4.0% : fill 30min 5% · séance 11% (18/152) · gap 2% · délai 50.2min · rebond 55% (9/18) (MFE +1.38%)
   - −5.0% : fill 30min 2% · séance 6% (10/152) · gap 2% · délai 110.1min · rebond 80% (8/10) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −1.9%) → stop au-delà de −1.45% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.92% (p90 −2.11%) → stop au-delà de −1.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.13%) → stop au-delà de −1.69% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=396 jambes) : jambe baissière méd −1.07% (p90 −2.65%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (43/44) · rebond 63% (24/43)
      · −2.0% : fill 69% (32/44) · rebond 72% (17/32)
      · −3.0% : fill 26% (18/44) · rebond 44% (9/18)
      · −4.0% : fill 18% (10/44) · rebond 58% (5/10)
      · −5.0% : fill 10% (6/44) · rebond 100% (6/6)
   - **flat** (41 séances) :
      · −1.0% : fill 66% (27/41) · rebond 42% (8/27)
      · −2.0% : fill 36% (14/41) · rebond 30% (6/14)
      · −3.0% : fill 27% (10/41) · rebond 50% (6/10)
      · −4.0% : fill 12% (5/41) · rebond 60% (3/5)
      · −5.0% : fill 5% (2/41) · rebond 55% (1/2)
   - **gap-up** (67 séances) :
      · −1.0% : fill 36% (20/67) · rebond 54% (12/20)
      · −2.0% : fill 18% (12/67) · rebond 67% (8/12)
      · −3.0% : fill 7% (6/67) · rebond 42% (2/6)
      · −4.0% : fill 5% (3/67) · rebond 38% (1/3)
      · −5.0% : fill 3% (2/67) · rebond 52% (1/2)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 77% si les 15 1res min sont vertes (54 cas) · 29% si rouges (106 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **24min** → P(séance verte=clôture>ouverture) 80% si début vert vs 23% si rouge (base 46% · écart 57 pts) ; prédictivité sature ensuite (plafond brut 220min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=61) : tient le vert **80%** · continue >prix actuel 50% ; creux résiduel méd -1.09% (q20 -1.92%) → **SL/trailing à −1.92%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.13% / q75 +2.34% → **scale +1.13% / runner +2.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=99) : edge inversé — récupère vert seulement **23%** (continue à baisser 57%) → **RÉDUIRE ~77%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.24%** (au-delà de la MAE q10 -3.24%), cible rebond +0.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.05% .. +2.37%] · haut q95 +2.79% · bas q05 -3.49%
   - 60min (n=160) : retour [-3.26% .. +2.25%] · haut q95 +3.1% · bas q05 -3.79%
   - 2h (n=160) : retour [-3.3% .. +2.93%] · haut q95 +4.01% · bas q05 -4.39%
   - 4h (n=160) : retour [-3.32% .. +2.6%] · haut q95 +4.13% · bas q05 -4.77%
   - 6h (n=160) : retour [-3.97% .. +3.19%] · haut q95 +4.57% · bas q05 -5.01%
   - session (n=160) : retour [-3.88% .. +3.14%] · haut q95 +4.57% · bas q05 -5.01%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 207940 = **plat / peu volatil** (vol intra méd 1.99%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 43.1  _(momentum baissier)_
- **ADX** : 23.3  _(pas de tendance nette)_
- **MACD** : hist 1039.397  _(bullish_recent)_
- **BB** : %B 0.53 · largeur 9.6%
- **ATR** : 33489.48 (11.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.036  _(neutre)_
- **Vol ratio** : 1.53  _(volume au-dessus de la moyenne)_
- **Choppiness** : 65.2  _(marche en range (choppy))_
- **MA** : MA20 1420797.82 · MA50 1480779.13 · MA200 1550724.78  _(prix > MA20)_
- **Dist MA** : MA20 +0.3% · MA50 -3.8% · MA200 -8.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (547730 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
