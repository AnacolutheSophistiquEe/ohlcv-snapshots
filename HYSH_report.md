# 298040

**Generated** : 2026-07-10T21:53:51.820796+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩2924000.00  

> 🟡 **WAIT-FOR-DIP** — spot +2.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2924000.00 (+2.2% vs entrée) · entrée ₩2860750.00 · stop ₩2763635.71 · T1 ₩3040348.84 · R/R 1.85  
> ↳ P(T1 av. stop) 24 % · EV/risk 0.16 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2842255.79–₩2879244.21 (mid ₩2860750.00)
- Spot actuel : ₩2924000.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : ₩2763635.71 (stop swing_plan-based (-8.19%))
- Targets : T1 ₩3040348.84 · R/R 1.85 | T2 ₩3088835.68 · R/R 2.35 | T3 ₩3137322.53 · R/R 2.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2763635.71


## Edge, scénarios & sizing

- EV/risk : 0.16 | EV/share : ₩15565.114 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 13 % | T3 8 %
- Kelly (position) : f* 0.028 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.3 | bear 55.0 | side 36.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.6  _(momentum baissier)_
- **ADX** : 13.6  _(pas de tendance nette)_
- **MACD** : hist -68865.691  _(pas de croisement recent)_
- **BB** : %B 0.2 · largeur 45.2%
- **ATR** : 323714.29 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.243  _(distribution)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 41.2  _(transition)_
- **MA** : MA20 3391000.0 · MA50 3652480.0 · MA200 2562193.72  _(prix < MA20)_
- **Dist MA** : MA20 -13.8% · MA50 -19.9% · MA200 +14.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16549 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
