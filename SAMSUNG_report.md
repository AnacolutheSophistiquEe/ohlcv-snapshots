# 005930

**Generated** : 2026-07-13T21:50:46.169080+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩259500.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩259500.00 (+8.5% vs entrée) · entrée ₩239171.66 · stop ₩230070.75 · T1 ₩257373.49 · R/R 2.0  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.618 · ¼-Kelly 0.03 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -58 % hors [0,100] (R² max 0.97). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩235531.30–₩242812.03 (mid ₩239171.66)
- Spot actuel : ₩259500.00 (+8.5% au-dessus de la zone — repli à attendre)
- Stop : ₩230070.75 (stop swing_plan-based (-11.34%))
- Targets : T1 ₩257373.49 · R/R 2.0 | T2 ₩275575.32 · R/R 4.0 | T3 ₩293777.14 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩230070.75


## Edge, scénarios & sizing

- EV/risk : 0.618 | EV/share : ₩5626.726 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 14 % | T3 3 %
- Kelly (position) : f* 0.119 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 50.7 | bear 7.4 | side 41.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.8  _(momentum baissier)_
- **ADX** : 19.4  _(pas de tendance nette)_
- **MACD** : hist -8845.806  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 38.8%
- **ATR** : 27821.43 (98.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.031  _(neutre)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 48.1  _(transition)_
- **MA** : MA20 319450.0 · MA50 304090.0 · MA200 182005.08  _(prix < MA20)_
- **Dist MA** : MA20 -18.8% · MA50 -14.7% · MA200 +42.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17220 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
