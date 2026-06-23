# AL2SI

**Generated** : 2026-06-23T21:43:05.899816+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 14.9 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · €27.62  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €27.62 (+15.3% vs entrée) · entrée €23.96 · stop €22.05 · T1 €25.93 · R/R 1.03  
> ↳ P(T1 av. stop) 21 % · EV/risk -0.014 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €23.66–€24.26 (mid €23.96)
- Spot actuel : €27.62 (+15.3% au-dessus de la zone — repli à attendre)
- Stop : €22.05 (stop swing_plan-based (-36.13%))
- Targets : T1 €25.93 · R/R 1.03 | T2 €27.89 · R/R 2.06 | T3 €29.85 · R/R 3.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €22.05


## Edge, scénarios & sizing

- EV/risk : -0.014 | EV/share : €-0.027 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 21 % | T2 3 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 25.0 | bear 46.6 | side 28.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 138.0 (= 5 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→85% · +1.0%→79% · +2.0%→75% · +3.0%→64% · +5.0%→40% · +8.0%→20%
- Range intraday médian 7.78% (p90 13.46%) · excursion haute méd. +3.92% / basse méd. −3.43%
- Profil de vol intra : ouverture 5.218% vs midi 1.539% vs clôture 1.821% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.167 ; neutre — autocorr -0.028)_ ; drift intra méd. 0.038% ; recovery-V 34%
- **σ réalisé intraday** 7.447% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 65% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 20.2904 (VA 16.5149–22.1781 ; dernier close 22.56)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.12 · part idiosyncratique 0.89
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.4  _(survente)_
- **ADX** : 30.5  _(tendance etablie)_
- **MACD** : hist -3.636  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 98.2%
- **ATR** : 6.44 (100.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF 0.029  _(neutre)_
- **Vol ratio** : 3.2  _(volume au-dessus de la moyenne)_
- **Choppiness** : 29.4  _(marche directionnel)_
- **MA** : MA20 45.88 · MA50 42.24 · MA200 22.11  _(prix < MA20)_
- **Dist MA** : MA20 -39.8% · MA50 -34.6% · MA200 +24.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (26522 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
