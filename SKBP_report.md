# 326030

**Generated** : 2026-07-14T21:56:58.644408+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩75100.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩75100.00 (+7.5% vs entrée) · entrée ₩69828.57 · stop ₩68247.14 · T1 ₩71307.09 · R/R 0.93  
> ↳ P(T1 av. stop) 32 % · EV/risk -0.079 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -22 % hors [0,100] (R² max 0.61). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩69532.87–₩70124.27 (mid ₩69828.57)
- Spot actuel : ₩75100.00 (+7.5% au-dessus de la zone — repli à attendre)
- Stop : ₩68247.14 (stop swing_plan-based (-16.14%))
- Targets : T1 ₩71307.09 · R/R 0.93 | T2 ₩72785.61 · R/R 1.87 | T3 ₩74264.12 · R/R 2.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩68247.14


## Edge, scénarios & sizing

- EV/risk : -0.079 | EV/share : ₩-125.340 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 32 % | T2 14 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 18.8 | bear 74.2 | side 7.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 35.0  _(momentum baissier)_
- **ADX** : 11.4  _(pas de tendance nette)_
- **MACD** : hist -689.219  _(pas de croisement recent)_
- **BB** : %B -0.12 · largeur 18.4%
- **ATR** : 5271.43 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.113  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 84855.0 · MA50 90236.0 · MA200 107819.0  _(prix < MA20)_
- **Dist MA** : MA20 -11.5% · MA50 -16.8% · MA200 -30.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16580 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
