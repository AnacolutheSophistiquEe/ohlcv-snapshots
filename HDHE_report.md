# 267260

**Generated** : 2026-07-10T00:16:06.009523+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩815000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩815000.00 (+2.3% vs entrée) · entrée ₩796413.71 · stop ₩769863.71 · T1 ₩832775.15 · R/R 1.37  
> ↳ P(T1 av. stop) 28 % · EV/risk 0.053 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩791963.01–₩800864.42 (mid ₩796413.71)
- Spot actuel : ₩815000.00 (+2.3% au-dessus de la zone — repli à attendre)
- Stop : ₩769863.71 (stop swing_plan-based (-8.27%))
- Targets : T1 ₩832775.15 · R/R 1.37 | T2 ₩847873.58 · R/R 1.94 | T3 ₩862972.02 · R/R 2.51
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩769863.71


## Edge, scénarios & sizing

- EV/risk : 0.053 | EV/share : ₩1401.144 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 28 % | T2 12 % | T3 7 %
- Kelly (position) : f* 0.006 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.4 | bear 79.7 | side 11.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 26.0  _(survente)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -13471.015  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 42.5%
- **ATR** : 88500.0 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.129  _(distribution)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 988350.0 · MA50 1090932.28 · MA200 908640.71  _(prix < MA20)_
- **Dist MA** : MA20 -17.5% · MA50 -25.3% · MA200 -10.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16369 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
