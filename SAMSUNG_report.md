# 005930

**Generated** : 2026-07-06T21:45:39.220739+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite extreme · ₩309500.00  

> 🟡 **WAIT-FOR-DIP** — spot +0.7 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩309500.00 (+0.7% vs entrée) · entrée ₩307475.79 · stop ₩299627.58 · T1 ₩318922.85 · R/R 1.46  
> ↳ P(T1 av. stop) 29 % · EV/risk 0.275 · ¼-Kelly 0.01 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩305451.58–₩309500.00 (mid ₩307475.79)
- Spot actuel : ₩309500.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : ₩299627.58 (stop swing_plan-based (-12.31%))
- Targets : T1 ₩318922.85 · R/R 1.46 | T2 ₩330369.92 · R/R 2.92 | T3 ₩341816.98 · R/R 4.38
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩299627.58


## Edge, scénarios & sizing

- EV/risk : 0.275 | EV/share : ₩2160.910 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 29 % | T2 10 % | T3 3 %
- Kelly (position) : f* 0.04 | ¼-Kelly 0.01 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.8 | bear 13.1 | side 81.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 44.4  _(momentum baissier)_
- **ADX** : 19.1  _(pas de tendance nette)_
- **MACD** : hist -7486.921  _(pas de croisement recent)_
- **BB** : %B 0.3 · largeur 27.5%
- **ATR** : 26160.71 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.002  _(neutre)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 51.9  _(transition)_
- **MA** : MA20 327675.0 · MA50 296350.0 · MA200 175546.93  _(prix < MA20)_
- **Dist MA** : MA20 -5.5% · MA50 +4.4% · MA200 +76.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16160 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
