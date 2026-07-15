# 298040

**Generated** : 2026-07-15T21:54:06.936842+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩2869000.00  

> ⛔ **STAND-DOWN** — mise optimale nulle (Kelly ≤ 0) — edge trop ténu pour s'engager (EV blended à peine positive ; cf. badge pour la méthode/n des probas)  
> ↳ spot ₩2869000.00 (+1.8% vs entrée) · entrée ₩2819500.00 · stop ₩2709075.58 · T1 ₩3040348.84 · R/R 2.0  
> ↳ P(T1 av. stop) 14 % · EV/risk 0.106 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2801632.46–₩2837367.54 (mid ₩2819500.00)
- Spot actuel : ₩2869000.00 (+1.8% au-dessus de la zone — repli à attendre)
- Stop : ₩2709075.58 (stop swing_plan-based (-7.19%))
- Targets : T1 ₩3040348.84 · R/R 2.0 | T2 ₩3063524.88 · R/R 2.21 | T3 ₩3086700.93 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2709075.58


## Edge, scénarios & sizing

- EV/risk : 0.106 | EV/share : ₩11738.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 12 % | T3 9 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈212) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.1 | bear 54.0 | side 33.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 41.8  _(momentum baissier)_
- **ADX** : 14.8  _(pas de tendance nette)_
- **MACD** : hist -50535.213  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 48.9%
- **ATR** : 292428.57 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.246  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 41.6  _(transition)_
- **MA** : MA20 3226650.0 · MA50 3579320.0 · MA200 2582069.54  _(prix < MA20)_
- **Dist MA** : MA20 -11.1% · MA50 -19.8% · MA200 +11.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (16385 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
