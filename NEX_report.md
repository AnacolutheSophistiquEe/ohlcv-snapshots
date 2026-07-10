# NEX

**Generated** : 2026-07-10T21:43:38.303812+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · €134.00  

> 🟡 **WAIT-FOR-DIP** — spot +1.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €134.00 (+1.9% vs entrée) · entrée €131.53 · stop €129.98 · T1 €133.35 · R/R 1.17  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.031 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -24 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €131.17–€131.89 (mid €131.53)
- Spot actuel : €134.00 (+1.9% au-dessus de la zone — repli à attendre)
- Stop : €129.98 (stop swing_plan-based (-5.54%))
- Targets : T1 €133.35 · R/R 1.17 | T2 €135.17 · R/R 2.35 | T3 €136.99 · R/R 3.52
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.98


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : €0.049 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.9 | bear 57.9 | side 32.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.5  _(survente)_
- **ADX** : 30.2  _(tendance etablie)_
- **MACD** : hist -1.343  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 23.1%
- **ATR** : 5.17 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.11  _(distribution)_
- **Vol ratio** : 0.97  _(volume normal)_
- **Choppiness** : 38.1  _(marche directionnel)_
- **MA** : MA20 144.6 · MA50 152.2 · MA200 130.98  _(prix < MA20)_
- **Dist MA** : MA20 -7.3% · MA50 -12.0% · MA200 +2.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16227 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
