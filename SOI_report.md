# SOI

**Generated** : 2026-07-16T21:44:35.611695+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €90.18  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot €90.18 (+18.0% vs entrée) · entrée €76.42 · stop €73.30 · T1 €82.65 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.22 · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -385 % hors [0,100] (R² max 0.63). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €75.17–€77.67 (mid €76.42)
- Spot actuel : €90.18 (+18.0% au-dessus de la zone — repli à attendre)
- Stop : €73.30 (stop swing_plan-based (-18.71%))
- Targets : T1 €82.65 · R/R 2.0 | T2 €88.88 · R/R 3.99 | T3 €95.11 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €73.30


## Edge, scénarios & sizing

- EV/risk : 0.22 | EV/share : €0.686 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 19 % | T3 10 %
- Kelly (position) : f* 0.051 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 14.6 | bear 49.9 | side 35.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 90.0 (= 1 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
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

- **RSI** : 31.4  _(momentum baissier)_
- **ADX** : 17.7  _(pas de tendance nette)_
- **MACD** : hist -0.933  _(pas de croisement recent)_
- **BB** : %B 0.04 · largeur 37.8%
- **ATR** : 9.32 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.201  _(distribution)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 47.4  _(transition)_
- **MA** : MA20 109.25 · MA50 134.73 · MA200 67.79  _(prix < MA20)_
- **Dist MA** : MA20 -17.5% · MA50 -33.1% · MA200 +33.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (19251 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
