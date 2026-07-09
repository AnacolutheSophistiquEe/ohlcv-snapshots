# 000660

**Generated** : 2026-07-09T00:13:35.517297+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2076000.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2076000.00 (+1.0% vs entrée) · entrée ₩2055666.61 · stop ₩1972973.76 · T1 ₩2137716.98 · R/R 0.99  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.166 · ¼-Kelly 0.011 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2039256.54–₩2072076.69 (mid ₩2055666.61)
- Spot actuel : ₩2076000.00 (+1.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1972973.76 (stop swing_plan-based (-6.52%))
- Targets : T1 ₩2137716.98 · R/R 0.99 | T2 ₩2219767.35 · R/R 1.98 | T3 ₩2301817.72 · R/R 2.98
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1972973.76


## Edge, scénarios & sizing

- EV/risk : 0.166 | EV/share : ₩13709.213 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 13 % | T3 6 %
- Kelly (position) : f* 0.046 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.8 | bear 62.2 | side 30.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 36.9  _(momentum baissier)_
- **ADX** : 26.7  _(tendance etablie)_
- **MACD** : hist -90234.882  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 41.8%
- **ATR** : 275642.86 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.072  _(distribution)_
- **Vol ratio** : 1.17  _(volume normal)_
- **Choppiness** : 53.4  _(transition)_
- **MA** : MA20 2482300.0 · MA50 2105880.4 · MA200 1056870.85  _(prix < MA20)_
- **Dist MA** : MA20 -16.4% · MA50 -1.4% · MA200 +96.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16718 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
