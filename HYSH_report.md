# 298040

**Generated** : 2026-07-14T20:36:21.787651+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2658000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩2658000.00 (+2.1% vs entrée) · entrée ₩2602550.10 · stop ₩2512678.68 · T1 ₩2671000.00 · R/R 0.76  
> ↳ P(T1 av. stop) 47 % · EV/risk 0.04 · ¼-Kelly 0.003 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -48 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2588860.13–₩2616240.08 (mid ₩2602550.10)
- Spot actuel : ₩2658000.00 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : ₩2512678.68 (stop swing_plan-based (-7.97%))
- Targets : T1 ₩2671000.00 · R/R 0.76 | T2 ₩2752402.04 · R/R 1.67 | T3 ₩2833804.07 · R/R 2.57
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2512678.68


## Edge, scénarios & sizing

- EV/risk : 0.04 | EV/share : ₩3547.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 25 % | T3 11 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.0 | bear 77.5 | side 15.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : stretched_down
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

- **RSI** : 35.5  _(momentum baissier)_
- **ADX** : 14.8  _(pas de tendance nette)_
- **MACD** : hist -71111.611  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 50.1%
- **ATR** : 299571.43 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.297  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 3275000.0 · MA50 3599800.0 · MA200 2574719.15  _(prix < MA20)_
- **Dist MA** : MA20 -18.8% · MA50 -26.2% · MA200 +3.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17391 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
