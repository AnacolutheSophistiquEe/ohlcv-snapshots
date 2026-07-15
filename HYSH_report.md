# 298040

**Generated** : 2026-07-15T00:17:23.839443+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2677000.00  

> 🟢 **ARMED** — plan valide, prix dans/proche de la zone d'entrée — exécutable  
> ↳ spot ₩2677000.00 (+0.4% vs entrée) · entrée ₩2665035.50 · stop ₩2575164.07 · T1 ₩2744167.87 · R/R 0.88  
> ↳ P(T1 av. stop) 45 % · EV/risk 0.068 · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -46 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2653070.99–₩2677000.00 (mid ₩2665035.50)
- Spot actuel : ₩2677000.00 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : ₩2575164.07 (stop swing_plan-based (-4.17%))
- Targets : T1 ₩2744167.87 · R/R 0.88 | T2 ₩2823300.24 · R/R 1.76 | T3 ₩2902432.62 · R/R 2.64
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2575164.07


## Edge, scénarios & sizing

- EV/risk : 0.068 | EV/share : ₩6120.595 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 25 % | T3 11 %
- Kelly (position) : f* 0.039 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.0 | bear 77.5 | side 15.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 35.9  _(momentum baissier)_
- **ADX** : 14.8  _(pas de tendance nette)_
- **MACD** : hist -69899.076  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 49.9%
- **ATR** : 299571.43 (91.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.286  _(distribution)_
- **Vol ratio** : 0.91  _(volume normal)_
- **Choppiness** : 42.5  _(transition)_
- **MA** : MA20 3275950.0 · MA50 3600180.0 · MA200 2574814.15  _(prix < MA20)_
- **Dist MA** : MA20 -18.3% · MA50 -25.6% · MA200 +4.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16377 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
