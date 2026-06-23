# AL2SI

**Generated** : 2026-06-23T00:08:35.507931+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 13.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €25.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €25.40 (+36.8% vs entrée) · entrée €18.57 · stop €16.82 · T1 €21.68 · R/R 1.78  
> ↳ P(T1 av. stop) 36 % · EV/risk 0.032 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €18.05–€19.09 (mid €18.57)
- Spot actuel : €25.40 (+36.8% au-dessus de la zone — repli à attendre)
- Stop : €16.82 (stop atr-based (-34.52%))
- Targets : T1 €21.68 · R/R 1.78 | T2 €24.78 · R/R 3.55 | T3 €27.88 · R/R 5.32
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €16.82


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : €0.056 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 20 % | T3 10 %
- Kelly (position) : f* 0.001 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 43.0 | bear 39.1 | side 17.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 152.0 (= 6 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 131 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (trop peu de remplissages (2))
  - **swing** : indisponible (trop peu de remplissages (0))
  - **deep** : indisponible (trop peu de remplissages (0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→76% · +2.0%→67% · +3.0%→57% · +5.0%→37% · +8.0%→18%
- Range intraday médian 7.17% (p90 12.72%) · excursion haute méd. +3.55% / basse méd. −2.89%
- Profil de vol intra : ouverture 4.726% vs midi 1.472% vs clôture 1.75% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 16.2  _(survente)_
- **ADX** : 27.1  _(tendance etablie)_
- **MACD** : hist -3.384  _(pas de croisement recent)_
- **BB** : %B -0.17 · largeur 71.3%
- **ATR** : 5.85 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.103  _(distribution)_
- **Vol ratio** : 0.0  _(volume atone)_
- **Choppiness** : 32.2  _(marche directionnel)_
- **MA** : MA20 48.3 · MA50 42.74 · MA200 21.94  _(prix < MA20)_
- **Dist MA** : MA20 -47.4% · MA50 -40.6% · MA200 +15.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (24836 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
