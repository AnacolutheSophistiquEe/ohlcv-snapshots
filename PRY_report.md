# PRY

**Generated** : 2026-07-14T00:12:16.094692+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €132.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €132.70 (+7.5% vs entrée) · entrée €123.49 · stop €121.59 · T1 €127.28 · R/R 1.99  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.238 · ¼-Kelly 0.018 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -144 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €122.73–€124.25 (mid €123.49)
- Spot actuel : €132.70 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : €121.59 (stop swing_plan-based (-8.37%))
- Targets : T1 €127.28 · R/R 1.99 | T2 €131.07 · R/R 3.99 | T3 €134.87 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €121.59


## Edge, scénarios & sizing

- EV/risk : 0.238 | EV/share : €0.451 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 22 % | T3 6 %
- Kelly (position) : f* 0.073 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.8 | bear 38.3 | side 41.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 133.0 (= 1 part(s) × prix) · cible 160.0


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.0  _(survente)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist -1.575  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 17.7%
- **ATR** : 5.79 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.193  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 143.61 · MA50 146.3 · MA200 107.62  _(prix < MA20)_
- **Dist MA** : MA20 -7.6% · MA50 -9.3% · MA200 +23.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19833 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
