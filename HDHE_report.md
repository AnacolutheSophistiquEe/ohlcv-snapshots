# 267260

**Generated** : 2026-07-09T16:28:57.865979+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩822000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩822000.00 (+2.5% vs entrée) · entrée ₩801663.71 · stop ₩775113.71 · T1 ₩832775.15 · R/R 1.17  
> ↳ P(T1 av. stop) 32 % · EV/risk 0.039 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩797170.29–₩806157.13 (mid ₩801663.71)
- Spot actuel : ₩822000.00 (+2.5% au-dessus de la zone — repli à attendre)
- Stop : ₩775113.71 (stop swing_plan-based (-8.67%))
- Targets : T1 ₩832775.15 · R/R 1.17 | T2 ₩850817.95 · R/R 1.85 | T3 ₩868860.76 · R/R 2.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩775113.71


## Edge, scénarios & sizing

- EV/risk : 0.039 | EV/share : ₩1044.780 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 14 % | T3 7 %
- Kelly (position) : f* 0.005 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.4 | bear 79.7 | side 11.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 27.0  _(survente)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -13024.291  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 42.3%
- **ATR** : 88500.0 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.122  _(distribution)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 988700.0 · MA50 1091072.28 · MA200 908675.71  _(prix < MA20)_
- **Dist MA** : MA20 -16.9% · MA50 -24.7% · MA200 -9.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16653 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
