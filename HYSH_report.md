# 298040

**Generated** : 2026-07-13T21:35:22.230090+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 3/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2675000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩2675000.00 (+0.8% vs entrée) · entrée ₩2652911.47 · stop ₩2560918.61 · T1 ₩2832173.71 · R/R 1.95  
> ↳ P(T1 av. stop) 45 % · EV/risk 0.469 · ¼-Kelly 0.03 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -45 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 3/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2630822.94–₩2675000.00 (mid ₩2652911.47)
- Spot actuel : ₩2675000.00 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : ₩2560918.61 (stop swing_plan-based (-4.26%))
- Targets : T1 ₩2832173.71 · R/R 1.95 | T2 ₩3011435.95 · R/R 3.9 | T3 ₩3190698.19 · R/R 5.85
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2560918.61


## Edge, scénarios & sizing

- EV/risk : 0.469 | EV/share : ₩43136.456 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 26 % | T3 9 %
- Kelly (position) : f* 0.121 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.0 | bear 60.2 | side 28.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : stretched_down
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

- **RSI** : 32.2  _(momentum baissier)_
- **ADX** : 14.1  _(pas de tendance nette)_
- **MACD** : hist -72507.544  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 48.5%
- **ATR** : 306642.86 (93.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.31  _(distribution)_
- **Vol ratio** : 0.43  _(volume atone)_
- **Choppiness** : 46.4  _(transition)_
- **MA** : MA20 3337150.0 · MA50 3626460.0 · MA200 2568668.31  _(prix < MA20)_
- **Dist MA** : MA20 -19.8% · MA50 -26.2% · MA200 +4.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (17220 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
