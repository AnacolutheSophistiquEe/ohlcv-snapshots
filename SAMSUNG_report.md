# 005930

**Generated** : 2026-07-09T00:14:46.305740+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩277500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)  
> ↳ spot ₩277500.00 (+3.2% vs entrée) · entrée ₩268975.00 · stop ₩258640.59 · T1 ₩289643.83 · R/R 2.0  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.648 · ¼-Kelly 0.031 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -36 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩264841.23–₩273108.77 (mid ₩268975.00)
- Spot actuel : ₩277500.00 (+3.2% au-dessus de la zone — repli à attendre)
- Stop : ₩258640.59 (stop swing_plan-based (-6.8%))
- Targets : T1 ₩289643.83 · R/R 2.0 | T2 ₩310312.66 · R/R 4.0 | T3 ₩330981.48 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩258640.59


## Edge, scénarios & sizing

- EV/risk : 0.648 | EV/share : ₩6700.952 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.124 | ¼-Kelly 0.031 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 5.9 | bear 34.9 | side 59.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 34.1  _(momentum baissier)_
- **ADX** : 18.1  _(pas de tendance nette)_
- **MACD** : hist -8309.821  _(pas de croisement recent)_
- **BB** : %B 0.01 · largeur 30.2%
- **ATR** : 28482.14 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.024  _(neutre)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 52.0  _(transition)_
- **MA** : MA20 326250.0 · MA50 300960.0 · MA200 178967.79  _(prix < MA20)_
- **Dist MA** : MA20 -14.9% · MA50 -7.8% · MA200 +55.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17167 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
