# SRT3

**Generated** : 2026-06-23T21:37:19.366546+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €212.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €212.70 (+4.8% vs entrée) · entrée €203.02 · stop €200.12 · T1 €205.36 · R/R 0.81  
> ↳ P(T1 av. stop) 50 % · EV/risk -0.013 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €202.55–€203.49 (mid €203.02)
- Spot actuel : €212.70 (+4.8% au-dessus de la zone — repli à attendre)
- Stop : €200.12 (stop swing_plan-based (-10.47%))
- Targets : T1 €205.36 · R/R 0.81 | T2 €207.71 · R/R 1.62 | T3 €210.05 · R/R 2.42
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €200.12


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : €-0.037 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 28 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 61.5 | bear 10.2 | side 28.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=3, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→69% · +2.0%→42% · +3.0%→25% · +5.0%→8% · +8.0%→0%
- Range intraday médian 3.72% (p90 6.57%) · excursion haute méd. +1.78% / basse méd. −1.98%
- Profil de vol intra : ouverture 2.022% vs midi 0.915% vs clôture 1.029% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.119 ; neutre — autocorr 0.017)_ ; drift intra méd. -0.344% ; recovery-V 19%
- **σ réalisé intraday** 2.482% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 77% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 213.9062 (VA 213.0362–215.6463 ; dernier close 212.0)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.44 · part idiosyncratique 0.56
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 22.3  _(survente)_
- **ADX** : 17.5  _(pas de tendance nette)_
- **MACD** : hist -3.457  _(pas de croisement recent)_
- **BB** : %B 0.06 · largeur 19.4%
- **ATR** : 9.68 (85.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.218  _(distribution)_
- **Vol ratio** : 1.0  _(volume normal)_
- **Choppiness** : 43.4  _(transition)_
- **MA** : MA20 232.76 · MA50 226.98 · MA200 228.41  _(prix < MA20)_
- **Dist MA** : MA20 -8.6% · MA50 -6.3% · MA200 -6.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (23284 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
