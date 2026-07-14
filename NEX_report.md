# NEX

**Generated** : 2026-07-14T00:08:22.981813+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €133.20  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €133.20 (+1.7% vs entrée) · entrée €130.93 · stop €129.50 · T1 €132.71 · R/R 1.24  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.03 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈219) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €130.58–€131.29 (mid €130.93)
- Spot actuel : €133.20 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : €129.50 (stop swing_plan-based (-5.21%))
- Targets : T1 €132.71 · R/R 1.24 | T2 €134.48 · R/R 2.48 | T3 €136.26 · R/R 3.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €129.50


## Edge, scénarios & sizing

- EV/risk : 0.03 | EV/share : €0.043 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈219) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 40.1 | bear 47.2 | side 12.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.6  _(survente)_
- **ADX** : 31.7  _(tendance etablie)_
- **MACD** : hist -1.15  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 24.1%
- **ATR** : 4.78 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.066  _(distribution)_
- **Vol ratio** : 0.21  _(volume atone)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 143.85 · MA50 151.76 · MA200 131.02  _(prix < MA20)_
- **Dist MA** : MA20 -7.4% · MA50 -12.2% · MA200 +1.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16337 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
