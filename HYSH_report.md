# 298040

**Generated** : 2026-07-10T00:17:20.632614+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩2770000.00  

> 🟡 **WAIT-FOR-DIP** — spot +0.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2770000.00 (+0.9% vs entrée) · entrée ₩2745250.00 · stop ₩2649228.57 · T1 ₩2832627.03 · R/R 0.91  
> ↳ P(T1 av. stop) 43 % · EV/risk 0.074 · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2727774.59–₩2762725.41 (mid ₩2745250.00)
- Spot actuel : ₩2770000.00 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : ₩2649228.57 (stop swing_plan-based (-5.45%))
- Targets : T1 ₩2832627.03 · R/R 0.91 | T2 ₩2920004.06 · R/R 1.82 | T3 ₩3007381.08 · R/R 2.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2649228.57


## Edge, scénarios & sizing

- EV/risk : 0.074 | EV/share : ₩7117.852 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 23 % | T3 8 %
- Kelly (position) : f* 0.036 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.1 | bear 75.8 | side 17.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 28.1  _(survente)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist -80852.121  _(pas de croisement recent)_
- **BB** : %B 0.06 · largeur 43.0%
- **ATR** : 320071.43 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.277  _(distribution)_
- **Vol ratio** : 1.18  _(volume normal)_
- **Choppiness** : 40.7  _(transition)_
- **MA** : MA20 3413600.0 · MA50 3672820.0 · MA200 2554508.99  _(prix < MA20)_
- **Dist MA** : MA20 -18.9% · MA50 -24.6% · MA200 +8.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16453 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
