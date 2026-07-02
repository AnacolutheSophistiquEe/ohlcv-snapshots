# 005930

**Generated** : 2026-07-02T21:46:26.534819+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩286000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot ₩286000.00 (+4.8% vs entrée) · entrée ₩272800.00 · stop ₩261694.12 · T1 ₩295011.76 · R/R 2.0  
> ↳ P(T1 av. stop) 39 % · EV/risk 0.655 · ¼-Kelly 0.029 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -21 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩268357.65–₩277242.35 (mid ₩272800.00)
- Spot actuel : ₩286000.00 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : ₩261694.12 (stop swing_plan-based (-8.5%))
- Targets : T1 ₩295011.76 · R/R 2.0 | T2 ₩317223.51 · R/R 4.0 | T3 ₩339435.27 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩261694.12


## Edge, scénarios & sizing

- EV/risk : 0.655 | EV/share : ₩7272.950 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 12 % | T3 2 %
- Kelly (position) : f* 0.115 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.1 | bear 19.6 | side 75.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


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
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 42.3  _(momentum baissier)_
- **ADX** : 19.5  _(pas de tendance nette)_
- **MACD** : hist -7689.58  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 27.0%
- **ATR** : 25625.0 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.067  _(distribution)_
- **Vol ratio** : 1.26  _(volume normal)_
- **Choppiness** : 51.2  _(transition)_
- **MA** : MA20 328650.0 · MA50 294450.0 · MA200 174344.49  _(prix < MA20)_
- **Dist MA** : MA20 -13.0% · MA50 -2.9% · MA200 +64.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17802 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
