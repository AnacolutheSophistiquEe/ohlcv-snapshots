# 326030

**Generated** : 2026-07-15T21:58:26.408435+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩78600.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩78600.00 (+7.0% vs entrée) · entrée ₩73471.43 · stop ₩71932.86 · T1 ₩75121.57 · R/R 1.07  
> ↳ P(T1 av. stop) 30 % · EV/risk -0.069 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩73141.40–₩73801.46 (mid ₩73471.43)
- Spot actuel : ₩78600.00 (+7.0% au-dessus de la zone — repli à attendre)
- Stop : ₩71932.86 (stop swing_plan-based (-15.23%))
- Targets : T1 ₩75121.57 · R/R 1.07 | T2 ₩76771.71 · R/R 2.15 | T3 ₩78421.86 · R/R 3.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩71932.86


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : ₩-105.895 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 30 % | T2 13 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.0 | bear 81.3 | side 11.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 37.7  _(momentum baissier)_
- **ADX** : 12.9  _(pas de tendance nette)_
- **MACD** : hist -626.355  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 18.9%
- **ATR** : 5128.57 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.127  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 54.1  _(transition)_
- **MA** : MA20 84240.0 · MA50 89800.0 · MA200 107652.5  _(prix < MA20)_
- **Dist MA** : MA20 -6.7% · MA50 -12.5% · MA200 -27.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15170 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
