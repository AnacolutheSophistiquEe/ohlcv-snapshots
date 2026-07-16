# PRY

**Generated** : 2026-07-16T00:12:56.221182+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €134.40  

> 🟡 **WAIT-FOR-DIP** — spot +3.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €134.40 (+3.6% vs entrée) · entrée €129.79 · stop €128.03 · T1 €131.69 · R/R 1.08  
> ↳ P(T1 av. stop) 46 % · EV/risk 0.07 · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -27 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €129.41–€130.17 (mid €129.79)
- Spot actuel : €134.40 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : €128.03 (stop swing_plan-based (-9.06%))
- Targets : T1 €131.69 · R/R 1.08 | T2 €133.59 · R/R 2.16 | T3 €135.49 · R/R 3.24
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.03


## Edge, scénarios & sizing

- EV/risk : 0.07 | EV/share : €0.124 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 46 % | T2 23 % | T3 9 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 35.2 | bear 29.8 | side 35.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 134.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.4  _(momentum baissier)_
- **ADX** : 20.8  _(pas de tendance nette)_
- **MACD** : hist -1.053  _(pas de croisement recent)_
- **BB** : %B 0.19 · largeur 18.7%
- **ATR** : 5.87 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.14  _(distribution)_
- **Vol ratio** : 0.34  _(volume atone)_
- **Choppiness** : 54.4  _(transition)_
- **MA** : MA20 142.64 · MA50 146.09 · MA200 108.18  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -8.0% · MA200 +24.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18960 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
