# 000660

**Generated** : 2026-07-06T00:08:56.537924+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2425000.00  

> ⛔ **STAND-DOWN** — mise optimale nulle (Kelly ≤ 0) — edge trop ténu pour s'engager (EV blended à peine positive ; cf. badge pour la méthode/n des probas)  
> ↳ spot ₩2425000.00 (+0.6% vs entrée) · entrée ₩2410566.20 · stop ₩2265473.06 · T1 ₩2700752.48 · R/R 2.0  
> ↳ P(T1 av. stop) 6 % · EV/risk 0.199 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2396132.40–₩2425000.00 (mid ₩2410566.20)
- Spot actuel : ₩2425000.00 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : ₩2265473.06 (stop swing_plan-based (-13.05%))
- Targets : T1 ₩2700752.48 · R/R 2.0 | T2 ₩2716635.04 · R/R 2.11 | T3 ₩2732517.59 · R/R 2.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2265473.06


## Edge, scénarios & sizing

- EV/risk : 0.199 | EV/share : ₩28930.099 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 6 % | T2 5 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈211) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 48.6 | bear 28.3 | side 23.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 288.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 52.9  _(neutre)_
- **ADX** : 29.1  _(tendance etablie)_
- **MACD** : hist -59786.665  _(bearish_recent)_
- **BB** : %B 0.47 · largeur 47.0%
- **ATR** : 261285.71 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.028  _(neutre)_
- **Vol ratio** : 1.4  _(volume normal)_
- **Choppiness** : 51.4  _(transition)_
- **MA** : MA20 2460000.0 · MA50 2046908.13 · MA200 1027839.74  _(prix < MA20)_
- **Dist MA** : MA20 -1.4% · MA50 +18.5% · MA200 +135.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16514 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
