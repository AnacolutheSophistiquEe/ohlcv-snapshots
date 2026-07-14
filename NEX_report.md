# NEX

**Generated** : 2026-07-14T21:43:07.917038+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €135.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot €135.80 (+2.2% vs entrée) · entrée €132.88 · stop €131.43 · T1 €134.70 · R/R 1.26  
> ↳ P(T1 av. stop) 39 % · EV/risk 0.035 · ¼-Kelly 0.001 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -21 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €132.52–€133.25 (mid €132.88)
- Spot actuel : €135.80 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €131.43 (stop swing_plan-based (-6.19%))
- Targets : T1 €134.70 · R/R 1.26 | T2 €136.53 · R/R 2.52 | T3 €138.35 · R/R 3.77
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €131.43


## Edge, scénarios & sizing

- EV/risk : 0.035 | EV/share : €0.051 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 16 % | T3 4 %
- Kelly (position) : f* 0.003 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.8 | bear 42.8 | side 43.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 33.5  _(momentum baissier)_
- **ADX** : 31.6  _(tendance etablie)_
- **MACD** : hist -0.745  _(pas de croisement recent)_
- **BB** : %B 0.29 · largeur 24.3%
- **ATR** : 4.83 (83.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.017  _(neutre)_
- **Vol ratio** : 0.84  _(volume normal)_
- **Choppiness** : 46.1  _(transition)_
- **MA** : MA20 143.2 · MA50 151.37 · MA200 131.07  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -10.3% · MA200 +3.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16140 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
