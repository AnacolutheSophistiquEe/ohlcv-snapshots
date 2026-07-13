# NEX

**Generated** : 2026-07-13T21:43:43.013356+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €133.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €133.80 (+1.8% vs entrée) · entrée €131.38 · stop €129.95 · T1 €133.16 · R/R 1.24  
> ↳ P(T1 av. stop) 39 % · EV/risk 0.024 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈219) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €131.02–€131.74 (mid €131.38)
- Spot actuel : €133.80 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : €129.95 (stop swing_plan-based (-5.43%))
- Targets : T1 €133.16 · R/R 1.24 | T2 €134.95 · R/R 2.5 | T3 €136.73 · R/R 3.74
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.95


## Edge, scénarios & sizing

- EV/risk : 0.024 | EV/share : €0.034 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.001 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈219) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 40.4 | bear 46.9 | side 12.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 28.0  _(survente)_
- **ADX** : 31.7  _(tendance etablie)_
- **MACD** : hist -1.111  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 24.0%
- **ATR** : 4.78 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.032  _(neutre)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 143.88 · MA50 151.77 · MA200 131.02  _(prix < MA20)_
- **Dist MA** : MA20 -7.0% · MA50 -11.8% · MA200 +2.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16064 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
