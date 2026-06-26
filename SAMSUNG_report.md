# 005930

**Generated** : 2026-06-26T21:45:28.625703+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩339500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)  
> ↳ spot ₩339500.00 (+10.3% vs entrée) · entrée ₩307671.74 · stop ₩275382.61 · T1 ₩372250.00 · R/R 2.0  
> ↳ P(T1 av. stop) 16 % · EV/risk 0.041 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩302668.59–₩312674.88 (mid ₩307671.74)
- Spot actuel : ₩339500.00 (+10.3% au-dessus de la zone — repli à attendre)
- Stop : ₩275382.61 (stop swing_plan-based (-18.89%))
- Targets : T1 ₩372250.00 · R/R 2.0 | T2 ₩377370.75 · R/R 2.16 | T3 ₩382491.51 · R/R 2.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩275382.61


## Edge, scénarios & sizing

- EV/risk : 0.041 | EV/share : ₩1317.159 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 14 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 5.0 | bear 23.0 | side 72.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.16 · part idiosyncratique 0.84
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 59.4  _(momentum haussier)_
- **ADX** : 23.6  _(pas de tendance nette)_
- **MACD** : hist -2127.572  _(bearish_recent)_
- **BB** : %B 0.56 · largeur 25.4%
- **ATR** : 26214.29 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.087  _(accumulation)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 334675.0 · MA50 286320.0 · MA200 169421.39  _(prix > MA20)_
- **Dist MA** : MA20 +1.4% · MA50 +18.6% · MA200 +100.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18282 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
