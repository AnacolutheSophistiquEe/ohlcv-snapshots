# NEX

**Generated** : 2026-07-09T21:43:55.086814+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €132.80  

> 🟡 **WAIT-FOR-DIP** — spot +1.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €132.80 (+1.7% vs entrée) · entrée €130.63 · stop €129.06 · T1 €132.42 · R/R 1.14  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.033 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €130.27–€130.99 (mid €130.63)
- Spot actuel : €132.80 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €129.06 (stop swing_plan-based (-5.07%))
- Targets : T1 €132.42 · R/R 1.14 | T2 €134.22 · R/R 2.29 | T3 €136.01 · R/R 3.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.06


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : €0.051 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.007 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 36.7 | bear 50.5 | side 12.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
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

- **RSI** : 21.9  _(survente)_
- **ADX** : 28.7  _(tendance etablie)_
- **MACD** : hist -1.569  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 21.9%
- **ATR** : 5.25 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.163  _(distribution)_
- **Vol ratio** : 1.02  _(volume normal)_
- **Choppiness** : 33.7  _(marche directionnel)_
- **MA** : MA20 145.2 · MA50 152.63 · MA200 130.95  _(prix < MA20)_
- **Dist MA** : MA20 -8.5% · MA50 -13.0% · MA200 +1.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16301 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
