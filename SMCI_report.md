# SMCI

**Generated** : 2026-06-23T21:48:57.935002+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · $33.32  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $33.32 (+14.1% vs entrée) · entrée $29.19 · stop $27.95 · T1 $30.87 · R/R 1.35  
> ↳ P(T1 av. stop) 15 % · EV/risk 0.023 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $28.85–$29.52 (mid $29.19)
- Spot actuel : $33.32 (+14.1% au-dessus de la zone — repli à attendre)
- Stop : $27.95 (stop swing_plan-based (-29.66%))
- Targets : T1 $30.87 · R/R 1.35 | T2 $32.56 · R/R 2.72 | T3 $34.24 · R/R 4.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $27.95


## Edge, scénarios & sizing

- EV/risk : 0.023 | EV/share : $0.029 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 1 % | T3 0 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 11.9 | bear 11.3 | side 76.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→81% · +2.0%→66% · +3.0%→48% · +5.0%→31% · +8.0%→12%
- Range intraday médian 6.17% (p90 10.16%) · excursion haute méd. +2.92% / basse méd. −2.54%
- Profil de vol intra : ouverture 3.625% vs midi 1.274% vs clôture 1.439% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.169 ; neutre — autocorr 0.003)_ ; drift intra méd. 0.727% ; recovery-V 32%
- **σ réalisé intraday** 4.407% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 57% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 35.3487 (VA 34.8113–36.2087 ; dernier close 35.46)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.41 · part idiosyncratique 0.59
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.4  _(momentum baissier)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist -1.03  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 76.9%
- **ATR** : 4.13 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.003  _(neutre)_
- **Vol ratio** : 0.73  _(volume normal)_
- **Choppiness** : 36.1  _(marche directionnel)_
- **MA** : MA20 37.97 · MA50 33.21 · MA200 35.49  _(prix < MA20)_
- **Dist MA** : MA20 -12.2% · MA50 +0.3% · MA200 -6.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (23493 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
