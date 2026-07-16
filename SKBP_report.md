# 326030

**Generated** : 2026-07-16T00:21:57.550241+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩78200.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩78200.00 (+7.0% vs entrée) · entrée ₩73071.43 · stop ₩71532.86 · T1 ₩74697.60 · R/R 1.06  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.069 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩72746.19–₩73396.66 (mid ₩73071.43)
- Spot actuel : ₩78200.00 (+7.0% au-dessus de la zone — repli à attendre)
- Stop : ₩71532.86 (stop swing_plan-based (-15.28%))
- Targets : T1 ₩74697.60 · R/R 1.06 | T2 ₩76323.77 · R/R 2.11 | T3 ₩77949.94 · R/R 3.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩71532.86


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : ₩-106.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 13 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.0 | bear 81.4 | side 11.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 37.1  _(momentum baissier)_
- **ADX** : 12.9  _(pas de tendance nette)_
- **MACD** : hist -651.882  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 19.1%
- **ATR** : 5128.57 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.135  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 54.1  _(transition)_
- **MA** : MA20 84220.0 · MA50 89792.0 · MA200 107650.5  _(prix < MA20)_
- **Dist MA** : MA20 -7.1% · MA50 -12.9% · MA200 -27.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15475 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
