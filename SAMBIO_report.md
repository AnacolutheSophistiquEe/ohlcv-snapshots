# 207940

**Generated** : 2026-07-15T21:57:01.440385+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1396000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1396000.00 (+2.5% vs entrée) · entrée ₩1362500.00 · stop ₩1340492.86 · T1 ₩1391814.62 · R/R 1.33  
> ↳ P(T1 av. stop) 26 % · EV/risk -0.03 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1356637.08–₩1368362.92 (mid ₩1362500.00)
- Spot actuel : ₩1396000.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : ₩1340492.86 (stop swing_plan-based (-7.56%))
- Targets : T1 ₩1391814.62 · R/R 1.33 | T2 ₩1421129.25 · R/R 2.66 | T3 ₩1450443.87 · R/R 4.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1340492.86


## Edge, scénarios & sizing

- EV/risk : -0.03 | EV/share : ₩-658.069 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 10 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 70.5 | bear 7.5 | side 22.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


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

- **RSI** : 51.0  _(neutre)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist 1585.656  _(pas de croisement recent)_
- **BB** : %B 0.58 · largeur 12.7%
- **ATR** : 73357.14 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.025  _(neutre)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 71.4  _(marche en range (choppy))_
- **MA** : MA20 1381100.0 · MA50 1380340.0 · MA200 1617402.66  _(prix > MA20)_
- **Dist MA** : MA20 +1.1% · MA50 +1.1% · MA200 -13.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15210 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
