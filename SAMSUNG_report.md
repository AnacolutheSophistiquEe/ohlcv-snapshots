# 005930

**Generated** : 2026-07-13T00:14:45.469746+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩285000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩285000.00 (+2.1% vs entrée) · entrée ₩279250.00 · stop ₩267625.00 · T1 ₩302500.00 · R/R 2.0  
> ↳ P(T1 av. stop) 7 % · EV/risk 0.166 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩277398.91–₩281101.09 (mid ₩279250.00)
- Spot actuel : ₩285000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩267625.00 (stop swing_plan-based (-7.97%))
- Targets : T1 ₩302500.00 · R/R 2.0 | T2 ₩304716.09 · R/R 2.19 | T3 ₩306932.18 · R/R 2.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩267625.00


## Edge, scénarios & sizing

- EV/risk : 0.166 | EV/share : ₩1934.014 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 7 % | T2 6 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 85.3 | bear 5.9 | side 8.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


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

- **RSI** : 37.1  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -8024.974  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 34.3%
- **ATR** : 28107.14 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.024  _(neutre)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 53.9  _(transition)_
- **MA** : MA20 323325.0 · MA50 303340.0 · MA200 181070.43  _(prix < MA20)_
- **Dist MA** : MA20 -11.9% · MA50 -6.0% · MA200 +57.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16647 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
