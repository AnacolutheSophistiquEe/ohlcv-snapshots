# 207940

**Generated** : 2026-07-15T00:19:53.535846+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1368000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1368000.00 (+4.5% vs entrée) · entrée ₩1309700.00 · stop ₩1278021.81 · T1 ₩1373056.39 · R/R 2.0  
> ↳ P(T1 av. stop) 23 % · EV/risk -0.128 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1297028.72–₩1322371.28 (mid ₩1309700.00)
- Spot actuel : ₩1368000.00 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : ₩1278021.81 (stop swing_plan-based (-6.58%))
- Targets : T1 ₩1373056.39 · R/R 2.0 | T2 ₩1436412.78 · R/R 4.0 | T3 ₩1499769.16 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1278021.81


## Edge, scénarios & sizing

- EV/risk : -0.128 | EV/share : ₩-4040.551 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 23 % | T2 8 % | T3 1 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.0 | bear 7.9 | side 7.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 48.2  _(neutre)_
- **ADX** : 12.4  _(pas de tendance nette)_
- **MACD** : hist 910.352  _(pas de croisement recent)_
- **BB** : %B 0.43 · largeur 12.7%
- **ATR** : 74571.43 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.009  _(neutre)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 72.0  _(marche en range (choppy))_
- **MA** : MA20 1379800.0 · MA50 1381820.0 · MA200 1618417.84  _(prix < MA20)_
- **Dist MA** : MA20 -0.9% · MA50 -1.0% · MA200 -15.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15164 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
