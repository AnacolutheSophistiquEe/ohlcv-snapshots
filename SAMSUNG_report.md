# 005930

**Generated** : 2026-07-07T00:10:59.883892+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩318000.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩318000.00 (+1.2% vs entrée) · entrée ₩314125.00 · stop ₩306083.93 · T1 ₩325069.10 · R/R 1.36  
> ↳ P(T1 av. stop) 32 % · EV/risk 0.269 · ¼-Kelly 0.012 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩311936.18–₩316313.82 (mid ₩314125.00)
- Spot actuel : ₩318000.00 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : ₩306083.93 (stop swing_plan-based (-12.55%))
- Targets : T1 ₩325069.10 · R/R 1.36 | T2 ₩336013.20 · R/R 2.72 | T3 ₩346957.31 · R/R 4.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩306083.93


## Edge, scénarios & sizing

- EV/risk : 0.269 | EV/share : ₩2161.893 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 11 % | T3 3 %
- Kelly (position) : f* 0.049 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.7 | bear 13.0 | side 81.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 44.9  _(momentum baissier)_
- **ADX** : 18.2  _(pas de tendance nette)_
- **MACD** : hist -6529.636  _(pas de croisement recent)_
- **BB** : %B 0.37 · largeur 26.0%
- **ATR** : 26803.57 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.065  _(accumulation)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 328800.0 · MA50 298330.0 · MA200 176790.4  _(prix < MA20)_
- **Dist MA** : MA20 -3.3% · MA50 +6.6% · MA200 +79.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16294 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
