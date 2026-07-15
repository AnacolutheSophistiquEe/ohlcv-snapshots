# NEX

**Generated** : 2026-07-15T21:43:45.426025+00:00  
**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · €136.00  

> ⛔ **STAND-DOWN** — mise optimale nulle (Kelly ≤ 0) — edge trop ténu pour s'engager (EV blended à peine positive ; cf. badge pour la méthode/n des probas)  
> ↳ spot €136.00 (+2.2% vs entrée) · entrée €133.09 · stop €131.65 · T1 €134.85 · R/R 1.22  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.024 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -21 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €132.74–€133.44 (mid €133.09)
- Spot actuel : €136.00 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : €131.65 (stop swing_plan-based (-6.12%))
- Targets : T1 €134.85 · R/R 1.22 | T2 €136.61 · R/R 2.44 | T3 €138.37 · R/R 3.67
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €131.65


## Edge, scénarios & sizing

- EV/risk : 0.024 | EV/share : €0.035 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 17 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.5 | bear 54.2 | side 31.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 35.8  _(momentum baissier)_
- **ADX** : 31.5  _(tendance etablie)_
- **MACD** : hist -0.427  _(pas de croisement recent)_
- **BB** : %B 0.31 · largeur 23.9%
- **ATR** : 4.79 (81.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.029  _(neutre)_
- **Vol ratio** : 1.23  _(volume normal)_
- **Choppiness** : 53.4  _(transition)_
- **MA** : MA20 142.34 · MA50 150.82 · MA200 131.13  _(prix < MA20)_
- **Dist MA** : MA20 -4.5% · MA50 -9.8% · MA200 +3.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (15445 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
