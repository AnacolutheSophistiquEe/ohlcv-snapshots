# SOI

**Generated** : 2026-07-15T00:09:48.403922+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €103.90  

> 🟡 **WAIT-FOR-DIP** — spot +10.3 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €103.90 (+10.3% vs entrée) · entrée €94.22 · stop €91.42 · T1 €97.63 · R/R 1.22  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.067 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €93.53–€94.90 (mid €94.22)
- Spot actuel : €103.90 (+10.3% au-dessus de la zone — repli à attendre)
- Stop : €91.42 (stop swing_plan-based (-23.73%))
- Targets : T1 €97.63 · R/R 1.22 | T2 €101.04 · R/R 2.44 | T3 €104.45 · R/R 3.65
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €91.42


## Edge, scénarios & sizing

- EV/risk : 0.067 | EV/share : €0.188 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.7 | bear 44.1 | side 47.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 104.0 (= 1 part(s) × prix) · cible 160.0


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 47.2  _(neutre)_
- **ADX** : 17.8  _(pas de tendance nette)_
- **MACD** : hist -0.658  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 33.3%
- **ATR** : 9.32 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.19  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 52.7  _(transition)_
- **MA** : MA20 111.98 · MA50 136.95 · MA200 67.25  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -24.1% · MA200 +54.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15716 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
