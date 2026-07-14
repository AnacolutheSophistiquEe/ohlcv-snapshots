# SOI

**Generated** : 2026-07-14T21:44:31.345725+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €102.75  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €102.75 (+10.1% vs entrée) · entrée €93.35 · stop €90.56 · T1 €96.70 · R/R 1.2  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.06 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €92.68–€94.02 (mid €93.35)
- Spot actuel : €102.75 (+10.1% au-dessus de la zone — repli à attendre)
- Stop : €90.56 (stop swing_plan-based (-23.33%))
- Targets : T1 €96.70 · R/R 1.2 | T2 €100.06 · R/R 2.41 | T3 €103.41 · R/R 3.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €90.56


## Edge, scénarios & sizing

- EV/risk : 0.06 | EV/share : €0.168 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.8 | bear 44.5 | side 46.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 103.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 46.2  _(neutre)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist -0.731  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 33.5%
- **ATR** : 9.32 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.179  _(distribution)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 52.7  _(transition)_
- **MA** : MA20 111.92 · MA50 136.93 · MA200 67.25  _(prix < MA20)_
- **Dist MA** : MA20 -8.2% · MA50 -25.0% · MA200 +52.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16619 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
