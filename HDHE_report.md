# 267260

**Generated** : 2026-07-14T00:15:59.857294+00:00  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩788000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩788000.00 (+1.5% vs entrée) · entrée ₩776163.71 · stop ₩747858.00 · T1 ₩832775.15 · R/R 2.0  
> ↳ P(T1 av. stop) 10 % · EV/risk 0.037 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.02). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩772250.80–₩780076.63 (mid ₩776163.71)
- Spot actuel : ₩788000.00 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : ₩747858.00 (stop swing_plan-based (-6.49%))
- Targets : T1 ₩832775.15 · R/R 2.0 | T2 ₩833727.35 · R/R 2.03 | T3 ₩834679.56 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩747858.00


## Edge, scénarios & sizing

- EV/risk : 0.037 | EV/share : ₩1059.849 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 10 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.6 | bear 75.0 | side 18.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 34.5  _(momentum baissier)_
- **ADX** : 20.2  _(pas de tendance nette)_
- **MACD** : hist -13769.549  _(pas de croisement recent)_
- **BB** : %B 0.08 · largeur 41.1%
- **ATR** : 83571.43 (84.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.324  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 50.9  _(transition)_
- **MA** : MA20 954100.0 · MA50 1072880.84 · MA200 911144.1  _(prix < MA20)_
- **Dist MA** : MA20 -17.4% · MA50 -26.6% · MA200 -13.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17043 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
