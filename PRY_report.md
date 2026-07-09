# PRY

**Generated** : 2026-07-09T00:12:20.037561+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €133.40  

> 🟡 **WAIT-FOR-DIP** — spot +3.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €133.40 (+3.4% vs entrée) · entrée €129.04 · stop €127.17 · T1 €130.94 · R/R 1.02  
> ↳ P(T1 av. stop) 48 % · EV/risk 0.09 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -125 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €128.66–€129.42 (mid €129.04)
- Spot actuel : €133.40 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : €127.17 (stop swing_plan-based (-8.73%))
- Targets : T1 €130.94 · R/R 1.02 | T2 €132.84 · R/R 2.03 | T3 €134.75 · R/R 3.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.17


## Edge, scénarios & sizing

- EV/risk : 0.09 | EV/share : €0.168 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 23 % | T3 8 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.3 | bear 31.3 | side 55.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 133.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 33.5  _(momentum baissier)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -1.68  _(pas de croisement recent)_
- **BB** : %B -0.07 · largeur 14.0%
- **ATR** : 6.23 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.09  _(distribution)_
- **Vol ratio** : 0.47  _(volume atone)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 145.02 · MA50 145.79 · MA200 106.84  _(prix < MA20)_
- **Dist MA** : MA20 -8.0% · MA50 -8.5% · MA200 +24.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19253 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
