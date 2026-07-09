# PRY

**Generated** : 2026-07-09T21:48:31.233170+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €136.55  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot €136.55 (+0.3% vs entrée) · entrée €136.14 · stop €134.29 · T1 €138.02 · R/R 1.02  
> ↳ P(T1 av. stop) 49 % · EV/risk 0.081 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -21 % hors [0,100] (R² max 0.86). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €135.77–€136.52 (mid €136.14)
- Spot actuel : €136.55 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : €134.29 (stop swing_plan-based (-1.99%))
- Targets : T1 €138.02 · R/R 1.02 | T2 €139.89 · R/R 2.03 | T3 €141.77 · R/R 3.04
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €134.29


## Edge, scénarios & sizing

- EV/risk : 0.081 | EV/share : €0.150 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 25 % | T3 10 %
- Kelly (position) : f* 0.029 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 20.9 | bear 36.0 | side 43.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 137.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 29.9  _(survente)_
- **ADX** : 18.1  _(pas de tendance nette)_
- **MACD** : hist -1.594  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 15.0%
- **ATR** : 6.16 (90.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.156  _(distribution)_
- **Vol ratio** : 0.78  _(volume normal)_
- **Choppiness** : 47.9  _(transition)_
- **MA** : MA20 144.69 · MA50 146.03 · MA200 107.11  _(prix < MA20)_
- **Dist MA** : MA20 -5.6% · MA50 -6.5% · MA200 +27.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19164 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
