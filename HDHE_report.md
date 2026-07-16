# 267260

**Generated** : 2026-07-16T00:16:53.342522+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩823000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩823000.00 (+2.6% vs entrée) · entrée ₩802413.71 · stop ₩777642.29 · T1 ₩832775.15 · R/R 1.23  
> ↳ P(T1 av. stop) 33 % · EV/risk 0.055 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩798357.91–₩806469.52 (mid ₩802413.71)
- Spot actuel : ₩823000.00 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : ₩777642.29 (stop swing_plan-based (-8.51%))
- Targets : T1 ₩832775.15 · R/R 1.23 | T2 ₩847920.80 · R/R 1.84 | T3 ₩863066.45 · R/R 2.45
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩777642.29


## Edge, scénarios & sizing

- EV/risk : 0.055 | EV/share : ₩1372.401 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 18 % | T3 9 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.5 | bear 75.3 | side 18.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 38.0  _(momentum baissier)_
- **ADX** : 21.8  _(pas de tendance nette)_
- **MACD** : hist -10071.461  _(pas de croisement recent)_
- **BB** : %B 0.22 · largeur 38.8%
- **ATR** : 82571.43 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.245  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 47.7  _(transition)_
- **MA** : MA20 923400.0 · MA50 1055088.8 · MA200 913333.77  _(prix < MA20)_
- **Dist MA** : MA20 -10.9% · MA50 -22.0% · MA200 -9.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16030 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
