# 005930

**Generated** : 2026-06-26T00:10:42.828139+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩358500.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (Kelly ≤ 0)  
> ↳ spot ₩358500.00 (+5.7% vs entrée) · entrée ₩339282.61 · stop ₩323923.91 · T1 ₩370000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 13 % · EV/risk 0.049 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩336856.76–₩341708.46 (mid ₩339282.61)
- Spot actuel : ₩358500.00 (+5.7% au-dessus de la zone — repli à attendre)
- Stop : ₩323923.91 (stop swing_plan-based (-15.31%))
- Targets : T1 ₩370000.00 · R/R 2.0 | T2 ₩372780.07 · R/R 2.18 | T3 ₩375560.15 · R/R 2.36
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩323923.91


## Edge, scénarios & sizing

- EV/risk : 0.049 | EV/share : ₩753.694 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 13 % | T2 11 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 14.9 | side 80.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 608.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.87
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.0  _(momentum haussier)_
- **ADX** : 25.4  _(tendance etablie)_
- **MACD** : hist -1494.976  _(bearish_recent)_
- **BB** : %B 0.79 · largeur 27.2%
- **ATR** : 26178.57 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.099  _(accumulation)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 332675.0 · MA50 283550.0 · MA200 168072.9  _(prix > MA20)_
- **Dist MA** : MA20 +7.8% · MA50 +26.4% · MA200 +113.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17277 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
