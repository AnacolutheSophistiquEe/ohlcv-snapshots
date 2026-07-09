# 326030

**Generated** : 2026-07-09T16:46:36.465266+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩80700.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩80700.00 (+7.5% vs entrée) · entrée ₩75078.57 · stop ₩73392.14 · T1 ₩76567.94 · R/R 0.88  
> ↳ P(T1 av. stop) 34 % · EV/risk -0.081 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩74780.70–₩75376.45 (mid ₩75078.57)
- Spot actuel : ₩80700.00 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : ₩73392.14 (stop swing_plan-based (-16.02%))
- Targets : T1 ₩76567.94 · R/R 0.88 | T2 ₩78057.31 · R/R 1.77 | T3 ₩79546.69 · R/R 2.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩73392.14


## Edge, scénarios & sizing

- EV/risk : -0.081 | EV/share : ₩-137.109 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 16 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.4 | bear 73.8 | side 5.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.6  _(momentum baissier)_
- **ADX** : 8.8  _(pas de tendance nette)_
- **MACD** : hist -228.416  _(bearish_recent)_
- **BB** : %B 0.01 · largeur 13.5%
- **ATR** : 5621.43 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.15  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 65.4  _(marche en range (choppy))_
- **MA** : MA20 86380.0 · MA50 91646.0 · MA200 108292.5  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 -11.9% · MA200 -25.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16013 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
