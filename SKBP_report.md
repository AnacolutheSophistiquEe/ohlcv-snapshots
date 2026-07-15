# 326030

**Generated** : 2026-07-15T00:21:05.661134+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩74600.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩74600.00 (+7.6% vs entrée) · entrée ₩69328.57 · stop ₩67747.14 · T1 ₩70813.46 · R/R 0.94  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.079 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.61). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩69031.59–₩69625.55 (mid ₩69328.57)
- Spot actuel : ₩74600.00 (+7.6% au-dessus de la zone — repli à attendre)
- Stop : ₩67747.14 (stop swing_plan-based (-16.25%))
- Targets : T1 ₩70813.46 · R/R 0.94 | T2 ₩72298.34 · R/R 1.88 | T3 ₩73783.23 · R/R 2.82
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩67747.14


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : ₩-124.689 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 31 % | T2 14 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.7 | bear 74.3 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.5  _(momentum baissier)_
- **ADX** : 11.4  _(pas de tendance nette)_
- **MACD** : hist -721.128  _(pas de croisement recent)_
- **BB** : %B -0.14 · largeur 18.8%
- **ATR** : 5271.43 (80.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.126  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 84830.0 · MA50 90226.0 · MA200 107816.5  _(prix < MA20)_
- **Dist MA** : MA20 -12.1% · MA50 -17.3% · MA200 -30.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15652 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
