# 000660

**Generated** : 2026-07-07T00:09:47.393218+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2343000.00  

> 🟡 **WAIT-FOR-DIP** — spot +3.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩2343000.00 (+3.9% vs entrée) · entrée ₩2255916.61 · stop ₩2175580.90 · T1 ₩2407000.00 · R/R 1.88  
> ↳ P(T1 av. stop) 19 % · EV/risk 0.276 · ¼-Kelly 0.005 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2236259.97–₩2275573.26 (mid ₩2255916.61)
- Spot actuel : ₩2343000.00 (+3.9% au-dessus de la zone — repli à attendre)
- Stop : ₩2175580.90 (stop swing_plan-based (-19.2%))
- Targets : T1 ₩2407000.00 · R/R 1.88 | T2 ₩2478436.40 · R/R 2.77 | T3 ₩2549872.81 · R/R 3.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2175580.90


## Edge, scénarios & sizing

- EV/risk : 0.276 | EV/share : ₩22131.690 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 7 % | T3 4 %
- Kelly (position) : f* 0.02 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 24.6 | bear 25.7 | side 49.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.2  _(neutre)_
- **ADX** : 27.7  _(tendance etablie)_
- **MACD** : hist -66440.154  _(pas de croisement recent)_
- **BB** : %B 0.37 · largeur 42.0%
- **ATR** : 267785.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.038  _(neutre)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 52.3  _(transition)_
- **MA** : MA20 2481600.0 · MA50 2069292.22 · MA200 1038230.86  _(prix < MA20)_
- **Dist MA** : MA20 -5.6% · MA50 +13.2% · MA200 +125.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16442 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
