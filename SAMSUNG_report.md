# 005930

**Generated** : 2026-07-01T00:10:52.019200+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩334000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩334000.00 (+2.4% vs entrée) · entrée ₩326125.00 · stop ₩309730.47 · T1 ₩358914.06 · R/R 2.0  
> ↳ P(T1 av. stop) 4 % · EV/risk 0.162 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩323873.17–₩328376.83 (mid ₩326125.00)
- Spot actuel : ₩334000.00 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : ₩309730.47 (stop swing_plan-based (-13.51%))
- Targets : T1 ₩358914.06 · R/R 2.0 | T2 ₩359357.07 · R/R 2.03 | T3 ₩359800.08 · R/R 2.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩309730.47


## Edge, scénarios & sizing

- EV/risk : 0.162 | EV/share : ₩2661.522 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 4 % | T2 4 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.9 | bear 11.6 | side 82.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.15 · part idiosyncratique 0.85
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.3  _(momentum haussier)_
- **ADX** : 20.7  _(pas de tendance nette)_
- **MACD** : hist -3844.908  _(pas de croisement recent)_
- **BB** : %B 0.5 · largeur 24.9%
- **ATR** : 25517.86 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.009  _(neutre)_
- **Vol ratio** : 0.93  _(volume normal)_
- **Choppiness** : 53.5  _(transition)_
- **MA** : MA20 334225.0 · MA50 291110.0 · MA200 172017.76  _(prix < MA20)_
- **Dist MA** : MA20 -0.1% · MA50 +14.7% · MA200 +94.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18796 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
