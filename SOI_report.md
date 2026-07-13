# SOI

**Generated** : 2026-07-13T00:09:41.170629+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €98.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €98.00 (+22.6% vs entrée) · entrée €79.94 · stop €76.72 · T1 €86.37 · R/R 2.0  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.249 · ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €78.65–€81.22 (mid €79.94)
- Spot actuel : €98.00 (+22.6% au-dessus de la zone — repli à attendre)
- Stop : €76.72 (stop swing_plan-based (-21.71%))
- Targets : T1 €86.37 · R/R 2.0 | T2 €92.80 · R/R 3.99 | T3 €99.23 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €76.72


## Edge, scénarios & sizing

- EV/risk : 0.249 | EV/share : €0.802 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.059 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 13.9 | bear 60.1 | side 26.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 98.0 (= 1 part(s) × prix) · cible 160.0


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

- **RSI** : 29.5  _(survente)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -1.292  _(pas de croisement recent)_
- **BB** : %B 0.1 · largeur 37.1%
- **ATR** : 10.62 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.245  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 59.2  _(transition)_
- **MA** : MA20 115.26 · MA50 139.14 · MA200 66.63  _(prix < MA20)_
- **Dist MA** : MA20 -15.0% · MA50 -29.6% · MA200 +47.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19191 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
