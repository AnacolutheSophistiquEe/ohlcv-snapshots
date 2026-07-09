# NEX

**Generated** : 2026-07-09T00:08:29.236402+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €130.20  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €130.20 (+1.2% vs entrée) · entrée €128.68 · stop €126.97 · T1 €130.45 · R/R 1.04  
> ↳ P(T1 av. stop) 41 % · EV/risk -0.009 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -241 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €128.33–€129.04 (mid €128.68)
- Spot actuel : €130.20 (+1.2% au-dessus de la zone — repli à attendre)
- Stop : €126.97 (stop swing_plan-based (-4.07%))
- Targets : T1 €130.45 · R/R 1.04 | T2 €132.22 · R/R 2.07 | T3 €134.00 · R/R 3.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €126.97


## Edge, scénarios & sizing

- EV/risk : -0.009 | EV/share : €-0.016 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 16 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈220) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.8 | bear 64.2 | side 16.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 25.4  _(survente)_
- **ADX** : 27.0  _(tendance etablie)_
- **MACD** : hist -1.667  _(pas de croisement recent)_
- **BB** : %B -0.02 · largeur 20.5%
- **ATR** : 5.71 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.134  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 32.2  _(marche directionnel)_
- **MA** : MA20 145.86 · MA50 152.97 · MA200 130.95  _(prix < MA20)_
- **Dist MA** : MA20 -10.7% · MA50 -14.9% · MA200 -0.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16491 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
