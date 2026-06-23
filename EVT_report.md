# EVT

**Generated** : 2026-06-23T00:04:42.301089+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €4.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €4.64 (+1.3% vs entrée) · entrée €4.58 · stop €4.53 · T1 €4.65 · R/R 1.4  
> ↳ P(T1 av. stop) 43 % · EV/risk 0.038 · ¼-Kelly 0.003 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.57–€4.60 (mid €4.58)
- Spot actuel : €4.64 (+1.3% au-dessus de la zone — repli à attendre)
- Stop : €4.53 (stop swing-based (-3.34%))
- Targets : T1 €4.65 · R/R 1.4 | T2 €4.71 · R/R 2.6 | T3 €4.78 · R/R 4.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.53


## Edge, scénarios & sizing

- EV/risk : 0.038 | EV/share : €0.002 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 21 % | T3 8 %
- Kelly (position) : f* 0.013 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 45.1 | bear 14.2 | side 40.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 162 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.096% → cible +1.418% / stop −1.136%, p_fill 67%, 109 remplis) : P(cible|rempli) **47%** · **EV/risk +0.008** (×p_fill ; si rempli +0.01% du capital)
  - **swing** (entrée dip −2.423% → cible +3.17% / stop −1.585%, p_fill 57%, 90 remplis) : P(cible|rempli) **34%** · **EV/risk -0.016** (×p_fill ; si rempli -0.04% du capital)
  - **deep** (entrée dip −3.743% → cible +4.482% / stop −2.241%, p_fill 53%, 81 remplis) : P(cible|rempli) **25%** · **EV/risk -0.172** (×p_fill ; si rempli -0.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→67% · +2.0%→39% · +3.0%→26% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.11% (p90 6.67%) · excursion haute méd. +1.66% / basse méd. −1.93%
- Profil de vol intra : ouverture 2.565% vs midi 1.146% vs clôture 1.185% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.15 · part idiosyncratique 0.31
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.5  _(momentum baissier)_
- **ADX** : 11.0  _(pas de tendance nette)_
- **MACD** : hist -0.027  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 18.8%
- **ATR** : 0.17 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.146  _(accumulation)_
- **Vol ratio** : 0.29  _(volume atone)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 4.88 · MA50 5.06 · MA200 5.58  _(prix < MA20)_
- **Dist MA** : MA20 -5.1% · MA50 -8.5% · MA200 -17.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (22567 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
