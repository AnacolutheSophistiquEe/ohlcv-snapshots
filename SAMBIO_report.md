# 207940

**Generated** : 2026-07-16T00:20:42.712950+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩1383000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩1383000.00 (+2.2% vs entrée) · entrée ₩1352750.00 · stop ₩1330742.86 · T1 ₩1381716.03 · R/R 1.32  
> ↳ P(T1 av. stop) 27 % · EV/risk -0.027 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1346956.79–₩1358543.21 (mid ₩1352750.00)
- Spot actuel : ₩1383000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩1330742.86 (stop swing_plan-based (-7.09%))
- Targets : T1 ₩1381716.03 · R/R 1.32 | T2 ₩1410682.06 · R/R 2.63 | T3 ₩1439648.09 · R/R 3.95
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1330742.86


## Edge, scénarios & sizing

- EV/risk : -0.027 | EV/share : ₩-585.034 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 10 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 71.6 | bear 7.4 | side 21.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.7  _(neutre)_
- **ADX** : 11.6  _(pas de tendance nette)_
- **MACD** : hist 756.026  _(pas de croisement recent)_
- **BB** : %B 0.51 · largeur 12.7%
- **ATR** : 73357.14 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.045  _(neutre)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 71.4  _(marche en range (choppy))_
- **MA** : MA20 1380450.0 · MA50 1380080.0 · MA200 1617337.66  _(prix > MA20)_
- **Dist MA** : MA20 +0.2% · MA50 +0.2% · MA200 -14.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15568 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
