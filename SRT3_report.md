# SRT3

**Generated** : 2026-06-23T00:03:22.041640+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €211.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €211.90 (+4.8% vs entrée) · entrée €202.25 · stop €199.35 · T1 €204.58 · R/R 0.8  
> ↳ P(T1 av. stop) 48 % · EV/risk -0.008 · ¼-Kelly 0.003 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €201.78–€202.72 (mid €202.25)
- Spot actuel : €211.90 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : €199.35 (stop atr-based (-6.83%))
- Targets : T1 €204.58 · R/R 0.8 | T2 €206.91 · R/R 1.61 | T3 €209.24 · R/R 2.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €199.35


## Edge, scénarios & sizing

- EV/risk : -0.008 | EV/share : €-0.024 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 22 % | T3 8 %
- Kelly (position) : f* 0.011 | ¼-Kelly 0.003 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 48.5 | bear 20.4 | side 31.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 164 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (trop peu de remplissages (7))
  - **swing** : indisponible (trop peu de remplissages (2))
  - **deep** : indisponible (trop peu de remplissages (1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→65% · +2.0%→36% · +3.0%→19% · +5.0%→5% · +8.0%→0%
- Range intraday médian 3.24% (p90 5.4%) · excursion haute méd. +1.49% / basse méd. −1.48%
- Profil de vol intra : ouverture 1.855% vs midi 0.828% vs clôture 0.863% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.41 · part idiosyncratique 0.23
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.4  _(survente)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist -3.548  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 17.8%
- **ATR** : 9.65 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.2  _(distribution)_
- **Vol ratio** : 0.31  _(volume atone)_
- **Choppiness** : 43.3  _(transition)_
- **MA** : MA20 233.72 · MA50 227.04 · MA200 228.28  _(prix < MA20)_
- **Dist MA** : MA20 -9.3% · MA50 -6.7% · MA200 -7.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (21088 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
