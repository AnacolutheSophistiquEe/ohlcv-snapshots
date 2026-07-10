# 326030

**Generated** : 2026-07-10T21:58:11.429211+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite high · ₩82400.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot ₩82400.00 (+0.5% vs entrée) · entrée ₩82000.00 · stop ₩80422.86 · T1 ₩83664.03 · R/R 1.06  
> ↳ P(T1 av. stop) 33 % · EV/risk -0.069 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩81667.19–₩82332.81 (mid ₩82000.00)
- Spot actuel : ₩82400.00 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : ₩80422.86 (stop swing_plan-based (-3.31%))
- Targets : T1 ₩83664.03 · R/R 1.06 | T2 ₩85328.07 · R/R 2.11 | T3 ₩86992.10 · R/R 3.17
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩80422.86


## Edge, scénarios & sizing

- EV/risk : -0.069 | EV/share : ₩-109.188 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 33 % | T2 16 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 23.5 | bear 69.6 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 46.0  _(neutre)_
- **ADX** : 9.2  _(pas de tendance nette)_
- **MACD** : hist -225.249  _(bearish_recent)_
- **BB** : %B 0.2 · largeur 14.2%
- **ATR** : 5257.14 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.116  _(distribution)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 65.1  _(marche en range (choppy))_
- **MA** : MA20 86080.0 · MA50 91236.0 · MA200 108154.5  _(prix < MA20)_
- **Dist MA** : MA20 -4.3% · MA50 -9.7% · MA200 -23.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16023 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
