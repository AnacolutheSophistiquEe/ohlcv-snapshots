# 267260

**Generated** : 2026-07-15T21:52:41.842967+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩829000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩829000.00 (+2.7% vs entrée) · entrée ₩806913.72 · stop ₩782142.29 · T1 ₩832775.15 · R/R 1.04  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.045 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩802797.71–₩811029.73 (mid ₩806913.72)
- Spot actuel : ₩829000.00 (+2.7% au-dessus de la zone — repli à attendre)
- Stop : ₩782142.29 (stop swing_plan-based (-8.85%))
- Targets : T1 ₩832775.15 · R/R 1.04 | T2 ₩850620.98 · R/R 1.76 | T3 ₩868466.82 · R/R 2.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩782142.29


## Edge, scénarios & sizing

- EV/risk : 0.045 | EV/share : ₩1104.171 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 21 % | T3 9 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 38.7  _(momentum baissier)_
- **ADX** : 21.8  _(pas de tendance nette)_
- **MACD** : hist -9688.555  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 38.7%
- **ATR** : 82571.43 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.235  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 47.7  _(transition)_
- **MA** : MA20 923700.0 · MA50 1055208.8 · MA200 913363.78  _(prix < MA20)_
- **Dist MA** : MA20 -10.3% · MA50 -21.4% · MA200 -9.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15775 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
