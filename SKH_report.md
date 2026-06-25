# 000660

**Generated** : 2026-06-25T00:09:54.066009+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 9/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2621000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)  
> ↳ spot ₩2621000.00 (+4.7% vs entrée) · entrée ₩2503300.00 · stop ₩2398921.18 · T1 ₩2712057.63 · R/R 2.0  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.107 · ¼-Kelly 0.006 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2461548.47–₩2545051.53 (mid ₩2503300.00)
- Spot actuel : ₩2621000.00 (+4.7% au-dessus de la zone — repli à attendre)
- Stop : ₩2398921.18 (stop swing_plan-based (-8.47%))
- Targets : T1 ₩2712057.63 · R/R 2.0 | T2 ₩2920815.26 · R/R 4.0 | T3 ₩3129572.89 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2398921.18


## Edge, scénarios & sizing

- EV/risk : 0.107 | EV/share : ₩11203.570 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.022 | ¼-Kelly 0.006 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 29.0 | bear 22.2 | side 48.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 640.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.3 · part idiosyncratique 0.69
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US Core PCE Price Index (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 57.5  _(momentum haussier)_
- **ADX** : 36.3  _(tendance etablie)_
- **MACD** : hist 18179.936  _(pas de croisement recent)_
- **BB** : %B 0.76 · largeur 43.7%
- **ATR** : 225785.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.04  _(neutre)_
- **Vol ratio** : 1.32  _(volume normal)_
- **Choppiness** : 40.3  _(transition)_
- **MA** : MA20 2355781.25 · MA50 1841182.2 · MA200 946800.97  _(prix > MA20)_
- **Dist MA** : MA20 +11.3% · MA50 +42.4% · MA200 +176.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18421 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
