# 298040

**Generated** : 2026-07-09T20:10:36.138646+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩2787000.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2787000.00 (+1.1% vs entrée) · entrée ₩2758000.00 · stop ₩2661978.57 · T1 ₩2846122.08 · R/R 0.92  
> ↳ P(T1 av. stop) 43 % · EV/risk 0.079 · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2740375.58–₩2775624.42 (mid ₩2758000.00)
- Spot actuel : ₩2787000.00 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : ₩2661978.57 (stop swing_plan-based (-5.78%))
- Targets : T1 ₩2846122.08 · R/R 0.92 | T2 ₩2934244.17 · R/R 1.84 | T3 ₩3022366.25 · R/R 2.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2661978.57


## Edge, scénarios & sizing

- EV/risk : 0.079 | EV/share : ₩7613.418 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 23 % | T3 8 %
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.1 | bear 75.8 | side 17.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 28.6  _(survente)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist -79767.221  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 42.8%
- **ATR** : 320071.43 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.272  _(distribution)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 40.7  _(transition)_
- **MA** : MA20 3414450.0 · MA50 3673160.0 · MA200 2554593.99  _(prix < MA20)_
- **Dist MA** : MA20 -18.4% · MA50 -24.1% · MA200 +9.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16584 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
