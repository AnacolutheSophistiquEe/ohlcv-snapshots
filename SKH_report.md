# 000660

**Generated** : 2026-07-09T15:54:22.534422+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2190000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2190000.00 (+2.3% vs entrée) · entrée ₩2141166.61 · stop ₩2058730.90 · T1 ₩2227528.24 · R/R 1.05  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.181 · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2123894.29–₩2158438.94 (mid ₩2141166.61)
- Spot actuel : ₩2190000.00 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : ₩2058730.90 (stop swing_plan-based (-9.19%))
- Targets : T1 ₩2227528.24 · R/R 1.05 | T2 ₩2313889.86 · R/R 2.1 | T3 ₩2400251.49 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2058730.90


## Edge, scénarios & sizing

- EV/risk : 0.181 | EV/share : ₩14948.506 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 13 % | T3 5 %
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 62.2 | side 30.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 37.8  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist -87248.263  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 40.7%
- **ATR** : 274785.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.091  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 2486750.0 · MA50 2125244.49 · MA200 1066384.77  _(prix < MA20)_
- **Dist MA** : MA20 -11.9% · MA50 +3.0% · MA200 +105.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16668 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
