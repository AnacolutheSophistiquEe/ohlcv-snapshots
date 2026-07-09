# 005930

**Generated** : 2026-07-09T20:07:31.451145+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩279250.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩279250.00 (+3.5% vs entrée) · entrée ₩269762.50 · stop ₩259394.87 · T1 ₩290497.76 · R/R 2.0  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.647 · ¼-Kelly 0.032 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -36 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩265615.45–₩273909.55 (mid ₩269762.50)
- Spot actuel : ₩279250.00 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : ₩259394.87 (stop swing_plan-based (-7.11%))
- Targets : T1 ₩290497.76 · R/R 2.0 | T2 ₩311233.02 · R/R 4.0 | T3 ₩331968.29 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩259394.87


## Edge, scénarios & sizing

- EV/risk : 0.647 | EV/share : ₩6708.070 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.126 | ¼-Kelly 0.032 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 9.8 | bear 6.2 | side 84.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 35.7  _(momentum baissier)_
- **ADX** : 18.5  _(pas de tendance nette)_
- **MACD** : hist -8587.364  _(pas de croisement recent)_
- **BB** : %B 0.06 · largeur 32.2%
- **ATR** : 28178.57 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.036  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 53.7  _(transition)_
- **MA** : MA20 325262.5 · MA50 302155.0 · MA200 180010.58  _(prix < MA20)_
- **Dist MA** : MA20 -14.1% · MA50 -7.6% · MA200 +55.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17164 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
