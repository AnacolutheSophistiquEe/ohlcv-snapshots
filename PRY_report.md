# PRY

**Generated** : 2026-07-13T00:12:15.411505+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €135.05  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot €135.05 (+3.7% vs entrée) · entrée €130.28 · stop €128.44 · T1 €132.07 · R/R 0.97  
> ↳ P(T1 av. stop) 49 % · EV/risk 0.082 · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €129.92–€130.63 (mid €130.28)
- Spot actuel : €135.05 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : €128.44 (stop swing_plan-based (-9.2%))
- Targets : T1 €132.07 · R/R 0.97 | T2 €133.86 · R/R 1.95 | T3 €135.65 · R/R 2.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.44


## Edge, scénarios & sizing

- EV/risk : 0.082 | EV/share : €0.150 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 26 % | T3 10 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 25.4 | bear 42.5 | side 32.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 135.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 26.2  _(survente)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -1.545  _(pas de croisement recent)_
- **BB** : %B 0.11 · largeur 16.2%
- **ATR** : 6.11 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.2  _(distribution)_
- **Vol ratio** : 0.6  _(volume atone)_
- **Choppiness** : 53.9  _(transition)_
- **MA** : MA20 144.25 · MA50 146.17 · MA200 107.37  _(prix < MA20)_
- **Dist MA** : MA20 -6.4% · MA50 -7.6% · MA200 +25.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19433 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
