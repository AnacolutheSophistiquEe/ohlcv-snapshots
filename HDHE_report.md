# 267260

**Generated** : 2026-07-10T21:52:28.071403+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩851000.00  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot ₩851000.00 (+0.5% vs entrée) · entrée ₩846443.79 · stop ₩819700.93 · T1 ₩868172.37 · R/R 0.81  
> ↳ P(T1 av. stop) 44 % · EV/risk 0.018 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩842098.07–₩850789.50 (mid ₩846443.79)
- Spot actuel : ₩851000.00 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : ₩819700.93 (stop swing_plan-based (-4.32%))
- Targets : T1 ₩868172.37 · R/R 0.81 | T2 ₩889900.95 · R/R 1.63 | T3 ₩911629.52 · R/R 2.44
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩819700.93


## Edge, scénarios & sizing

- EV/risk : 0.018 | EV/share : ₩493.656 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 24 % | T3 9 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.7 | bear 74.7 | side 18.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.1  _(momentum baissier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist -11823.352  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 42.6%
- **ATR** : 89142.86 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.194  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 974400.0 · MA50 1081857.21 · MA200 910112.04  _(prix < MA20)_
- **Dist MA** : MA20 -12.7% · MA50 -21.3% · MA200 -6.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16333 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
