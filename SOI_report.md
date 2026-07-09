# SOI

**Generated** : 2026-07-09T21:45:26.883811+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €104.10  

> 🟡 **WAIT-FOR-DIP** — spot +10.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €104.10 (+10.3% vs entrée) · entrée €94.36 · stop €91.07 · T1 €97.85 · R/R 1.06  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.035 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €93.67–€95.06 (mid €94.36)
- Spot actuel : €104.10 (+10.3% au-dessus de la zone — repli à attendre)
- Stop : €91.07 (stop swing_plan-based (-23.85%))
- Targets : T1 €97.85 · R/R 1.06 | T2 €101.33 · R/R 2.12 | T3 €104.81 · R/R 3.18
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €91.07


## Edge, scénarios & sizing

- EV/risk : 0.035 | EV/share : €0.117 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 19 % | T3 10 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.1 | bear 42.3 | side 47.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 104.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 41.2  _(momentum baissier)_
- **ADX** : 16.9  _(pas de tendance nette)_
- **MACD** : hist -1.188  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 37.4%
- **ATR** : 10.97 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.192  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 117.23 · MA50 139.72 · MA200 66.33  _(prix < MA20)_
- **Dist MA** : MA20 -11.2% · MA50 -25.5% · MA200 +56.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16281 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
