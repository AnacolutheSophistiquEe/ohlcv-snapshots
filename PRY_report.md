# PRY

**Generated** : 2026-07-15T00:12:23.350032+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €137.30  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot €137.30 (+0.3% vs entrée) · entrée €136.89 · stop €135.12 · T1 €138.84 · R/R 1.1  
> ↳ P(T1 av. stop) 47 % · EV/risk 0.086 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €136.50–€137.28 (mid €136.89)
- Spot actuel : €137.30 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €135.12 (stop swing_plan-based (-2.2%))
- Targets : T1 €138.84 · R/R 1.1 | T2 €140.79 · R/R 2.2 | T3 €142.74 · R/R 3.31
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €135.12


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : €0.153 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 23 % | T3 9 %
- Kelly (position) : f* 0.03 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 31.8 | bear 36.0 | side 32.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 137.0 (= 1 part(s) × prix) · cible 160.0


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 36.8  _(momentum baissier)_
- **ADX** : 20.5  _(pas de tendance nette)_
- **MACD** : hist -1.183  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 17.9%
- **ATR** : 5.9 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.166  _(distribution)_
- **Vol ratio** : 0.48  _(volume atone)_
- **Choppiness** : 51.5  _(transition)_
- **MA** : MA20 143.19 · MA50 146.27 · MA200 107.91  _(prix < MA20)_
- **Dist MA** : MA20 -4.1% · MA50 -6.1% · MA200 +27.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18414 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
