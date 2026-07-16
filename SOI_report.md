# SOI

**Generated** : 2026-07-16T00:10:14.686873+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €97.92  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot €97.92 (+22.6% vs entrée) · entrée €79.90 · stop €76.68 · T1 €86.35 · R/R 2.0  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.239 · ¼-Kelly 0.015 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €78.61–€81.19 (mid €79.90)
- Spot actuel : €97.92 (+22.6% au-dessus de la zone — repli à attendre)
- Stop : €76.68 (stop swing_plan-based (-21.7%))
- Targets : T1 €86.35 · R/R 2.0 | T2 €92.81 · R/R 4.01 | T3 €99.26 · R/R 6.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €76.68


## Edge, scénarios & sizing

- EV/risk : 0.239 | EV/share : €0.772 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 19 % | T3 11 %
- Kelly (position) : f* 0.059 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 16.9 | bear 49.3 | side 33.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.0  _(momentum baissier)_
- **ADX** : 17.4  _(pas de tendance nette)_
- **MACD** : hist -0.614  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 33.9%
- **ATR** : 9.07 (76.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.181  _(distribution)_
- **Vol ratio** : 0.72  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 110.58 · MA50 135.95 · MA200 67.54  _(prix < MA20)_
- **Dist MA** : MA20 -11.4% · MA50 -28.0% · MA200 +45.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (18857 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
