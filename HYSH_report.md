# 298040

**Generated** : 2026-07-14T00:17:13.227602+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2666000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩2666000.00 (+5.0% vs entrée) · entrée ₩2539610.23 · stop ₩2289240.93 · T1 ₩3040348.84 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % · EV/risk 0.198 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -46 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2505036.83–₩2574183.63 (mid ₩2539610.23)
- Spot actuel : ₩2666000.00 (+5.0% au-dessus de la zone — repli à attendre)
- Stop : ₩2289240.93 (stop swing_plan-based (-14.13%))
- Targets : T1 ₩3040348.84 · R/R 2.0 | T2 ₩3048494.29 · R/R 2.03 | T3 ₩3056639.75 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2289240.93


## Edge, scénarios & sizing

- EV/risk : 0.198 | EV/share : ₩49453.610 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 12 % | T2 10 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.0 | bear 60.2 | side 28.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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

- **RSI** : 32.1  _(momentum baissier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist -73081.903  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 48.6%
- **ATR** : 306642.86 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.316  _(distribution)_
- **Vol ratio** : 0.67  _(volume normal)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 3336700.0 · MA50 3626280.0 · MA200 2568623.31  _(prix < MA20)_
- **Dist MA** : MA20 -20.1% · MA50 -26.5% · MA200 +3.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17357 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
