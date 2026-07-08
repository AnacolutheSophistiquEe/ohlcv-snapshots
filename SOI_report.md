# SOI

**Generated** : 2026-07-08T18:41:30.286919+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €98.34  

> 🟡 **WAIT-FOR-DIP** — spot +9.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot €98.34 (+9.2% vs entrée) · entrée €90.05 · stop €86.79 · T1 €93.30 · R/R 1.0  
> ↳ P(T1 av. stop) 35 % · EV/risk 0.022 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -34 % hors [0,100] (R² max 0.94). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €89.39–€90.70 (mid €90.05)
- Spot actuel : €98.34 (+9.2% au-dessus de la zone — repli à attendre)
- Stop : €86.79 (stop swing_plan-based (-21.86%))
- Targets : T1 €93.30 · R/R 1.0 | T2 €96.56 · R/R 2.0 | T3 €99.81 · R/R 2.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €86.79


## Edge, scénarios & sizing

- EV/risk : 0.022 | EV/share : €0.072 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 10.7 | bear 45.3 | side 44.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 98.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 38.3  _(momentum baissier)_
- **ADX** : 16.9  _(pas de tendance nette)_
- **MACD** : hist -1.432  _(pas de croisement recent)_
- **BB** : %B 0.03 · largeur 36.4%
- **ATR** : 10.84 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.223  _(distribution)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 52.4  _(transition)_
- **MA** : MA20 118.45 · MA50 139.9 · MA200 66.0  _(prix < MA20)_
- **Dist MA** : MA20 -17.0% · MA50 -29.7% · MA200 +49.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18790 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
