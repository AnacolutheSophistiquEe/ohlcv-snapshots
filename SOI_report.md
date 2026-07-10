# SOI

**Generated** : 2026-07-10T00:09:45.550588+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €105.60  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot €105.60 (+0.5% vs entrée) · entrée €105.05 · stop €101.75 · T1 €108.97 · R/R 1.19  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.056 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €104.49–€105.60 (mid €105.05)
- Spot actuel : €105.60 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €101.75 (stop swing_plan-based (-5.12%))
- Targets : T1 €108.97 · R/R 1.19 | T2 €112.89 · R/R 2.38 | T3 €116.81 · R/R 3.56
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €101.75


## Edge, scénarios & sizing

- EV/risk : 0.056 | EV/share : €0.185 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 18 % | T3 10 %
- Kelly (position) : f* 0.001 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.0 | bear 40.3 | side 49.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 106.0 (= 1 part(s) × prix) · cible 160.0


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.2  _(momentum baissier)_
- **ADX** : 16.9  _(pas de tendance nette)_
- **MACD** : hist -1.092  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 37.1%
- **ATR** : 10.98 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.195  _(distribution)_
- **Vol ratio** : 0.23  _(volume atone)_
- **Choppiness** : 52.9  _(transition)_
- **MA** : MA20 117.3 · MA50 139.75 · MA200 66.34  _(prix < MA20)_
- **Dist MA** : MA20 -10.0% · MA50 -24.4% · MA200 +59.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18833 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
