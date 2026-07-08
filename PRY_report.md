# PRY

**Generated** : 2026-07-08T19:01:44.761431+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €133.30  

> 🟡 **WAIT-FOR-DIP** — spot +3.4 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €133.30 (+3.4% vs entrée) · entrée €128.96 · stop €127.09 · T1 €130.87 · R/R 1.02  
> ↳ P(T1 av. stop) 48 % · EV/risk 0.089 · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -126 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €128.58–€129.34 (mid €128.96)
- Spot actuel : €133.30 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : €127.09 (stop swing_plan-based (-8.69%))
- Targets : T1 €130.87 · R/R 1.02 | T2 €132.77 · R/R 2.04 | T3 €134.67 · R/R 3.05
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €127.09


## Edge, scénarios & sizing

- EV/risk : 0.089 | EV/share : €0.167 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 23 % | T3 8 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.2 | bear 31.4 | side 55.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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

- **RSI** : 33.4  _(momentum baissier)_
- **ADX** : 17.3  _(pas de tendance nette)_
- **MACD** : hist -1.687  _(pas de croisement recent)_
- **BB** : %B -0.08 · largeur 14.0%
- **ATR** : 6.23 (92.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.097  _(distribution)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 145.01 · MA50 145.79 · MA200 106.84  _(prix < MA20)_
- **Dist MA** : MA20 -8.1% · MA50 -8.6% · MA200 +24.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18910 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
