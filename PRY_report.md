# PRY

**Generated** : 2026-07-13T21:47:59.436926+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €133.35  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €133.35 (+7.7% vs entrée) · entrée €123.78 · stop €121.89 · T1 €127.57 · R/R 2.01  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.223 · ¼-Kelly 0.017 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -141 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €123.02–€124.54 (mid €123.78)
- Spot actuel : €133.35 (+7.7% au-dessus de la zone — repli à attendre)
- Stop : €121.89 (stop swing_plan-based (-8.6%))
- Targets : T1 €127.57 · R/R 2.01 | T2 €131.35 · R/R 4.01 | T3 €135.14 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €121.89


## Edge, scénarios & sizing

- EV/risk : 0.223 | EV/share : €0.422 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 22 % | T3 6 %
- Kelly (position) : f* 0.069 | ¼-Kelly 0.017 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 19.4 | bear 37.6 | side 43.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.6  _(survente)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist -1.534  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 17.6%
- **ATR** : 5.79 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.174  _(distribution)_
- **Vol ratio** : 0.83  _(volume normal)_
- **Choppiness** : 50.8  _(transition)_
- **MA** : MA20 143.64 · MA50 146.31 · MA200 107.63  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -8.9% · MA200 +23.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19694 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
