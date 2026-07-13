# 267260

**Generated** : 2026-07-13T21:33:57.786504+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩791000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩791000.00 (+1.6% vs entrée) · entrée ₩778413.72 · stop ₩751233.01 · T1 ₩832775.15 · R/R 2.0  
> ↳ P(T1 av. stop) 11 % · EV/risk 0.046 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -24 % hors [0,100] (R² max 0.02). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩774509.82–₩782317.62 (mid ₩778413.72)
- Spot actuel : ₩791000.00 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : ₩751233.01 (stop swing_plan-based (-6.67%))
- Targets : T1 ₩832775.15 · R/R 2.0 | T2 ₩834784.99 · R/R 2.07 | T3 ₩836794.82 · R/R 2.15
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩751233.01


## Edge, scénarios & sizing

- EV/risk : 0.046 | EV/share : ₩1252.273 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 11 % | T2 10 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.6 | bear 75.0 | side 18.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.7  _(momentum baissier)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist -13578.096  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 41.0%
- **ATR** : 83571.43 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.315  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 954250.0 · MA50 1072940.84 · MA200 911159.1  _(prix < MA20)_
- **Dist MA** : MA20 -17.1% · MA50 -26.3% · MA200 -13.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16901 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
