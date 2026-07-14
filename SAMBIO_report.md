# 207940

**Generated** : 2026-07-14T00:19:41.485476+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite extreme · ₩1400000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩1400000.00 (+2.5% vs entrée) · entrée ₩1365500.00 · stop ₩1341478.57 · T1 ₩1394727.48 · R/R 1.22  
> ↳ P(T1 av. stop) 28 % · EV/risk -0.015 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1359654.50–₩1371345.50 (mid ₩1365500.00)
- Spot actuel : ₩1400000.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : ₩1341478.57 (stop swing_plan-based (-7.68%))
- Targets : T1 ₩1394727.48 · R/R 1.22 | T2 ₩1423954.96 · R/R 2.43 | T3 ₩1453182.44 · R/R 3.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1341478.57


## Edge, scénarios & sizing

- EV/risk : -0.015 | EV/share : ₩-367.676 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 10 % | T3 4 %
- Kelly (position) : f* 0.005 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.0 | bear 6.2 | side 8.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.5  _(momentum haussier)_
- **ADX** : 12.8  _(pas de tendance nette)_
- **MACD** : hist 2600.927  _(pas de croisement recent)_
- **BB** : %B 0.62 · largeur 13.1%
- **ATR** : 80071.43 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.001  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 64.9  _(marche en range (choppy))_
- **MA** : MA20 1378050.0 · MA50 1383920.0 · MA200 1619557.66  _(prix > MA20)_
- **Dist MA** : MA20 +1.6% · MA50 +1.2% · MA200 -13.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16281 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
