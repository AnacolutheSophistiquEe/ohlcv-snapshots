# PRY

**Generated** : 2026-07-14T21:47:23.041686+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €137.85  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €137.85 (+0.4% vs entrée) · entrée €137.34 · stop €135.57 · T1 €139.31 · R/R 1.11  
> ↳ P(T1 av. stop) 47 % · EV/risk 0.09 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €136.94–€137.73 (mid €137.34)
- Spot actuel : €137.85 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : €135.57 (stop swing_plan-based (-2.41%))
- Targets : T1 €139.31 · R/R 1.11 | T2 €141.29 · R/R 2.23 | T3 €143.27 · R/R 3.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €135.57


## Edge, scénarios & sizing

- EV/risk : 0.09 | EV/share : €0.159 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 23 % | T3 9 %
- Kelly (position) : f* 0.031 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 32.6 | bear 36.2 | side 31.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 138.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.7  _(momentum baissier)_
- **ADX** : 20.5  _(pas de tendance nette)_
- **MACD** : hist -1.148  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 17.9%
- **ATR** : 5.9 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.143  _(distribution)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 143.22 · MA50 146.28 · MA200 107.91  _(prix < MA20)_
- **Dist MA** : MA20 -3.7% · MA50 -5.8% · MA200 +27.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19348 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
