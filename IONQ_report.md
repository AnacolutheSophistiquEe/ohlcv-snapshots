# IONQ

**Generated** : 2026-06-23T21:52:03.927083+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $57.85  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $57.85 (+4.0% vs entrée) · entrée $55.62 · stop $53.84 · T1 $57.44 · R/R 1.02  
> ↳ P(T1 av. stop) 50 % _(réel 5 s)_ · EV/risk 0.126 _(réel 5 s)_ (GBM -0.011) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $55.26–$55.98 (mid $55.62)
- Spot actuel : $57.85 (+4.0% au-dessus de la zone — repli à attendre)
- Stop : $53.84 (stop swing_plan-based (-11.83%))
- Targets : T1 $57.44 · R/R 1.02 | T2 $59.26 · R/R 2.04 | T3 $61.09 · R/R 3.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $53.84


## Edge, scénarios & sizing

- EV/risk : -0.011 | EV/share : $-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 17 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 11.6 | side 80.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 116.0 (= 2 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.856% → cible +3.275% / stop −3.198%, p_fill 52%, n_eff≈20.4) : P(cible|rempli) **50%** · **EV/risk +0.126** (×p_fill ; si rempli +0.77% du capital)
  - **swing** (entrée dip −8.479% → cible +7.323% / stop −3.662%, p_fill 36%, n_eff≈11.6) : P(cible|rempli) **33%** · **EV/risk -0.025** (×p_fill ; si rempli -0.25% du capital)
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=8))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→85% · +2.0%→69% · +3.0%→57% · +5.0%→30% · +8.0%→16%
- Range intraday médian 7.58% (p90 12.54%) · excursion haute méd. +3.58% / basse méd. −2.91%
- Profil de vol intra : ouverture 4.608% vs midi 1.613% vs clôture 1.683% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.023)_ ; drift intra méd. 0.667% ; recovery-V 46%
- **σ réalisé intraday** 5.35% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 48% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 59.7999 (VA 57.8709–60.6036 ; dernier close 58.32)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.36 · part idiosyncratique 0.64
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.0  _(momentum baissier)_
- **ADX** : 21.4  _(pas de tendance nette)_
- **MACD** : hist -1.182  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 37.6%
- **ATR** : 5.93 (89.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.086  _(distribution)_
- **Vol ratio** : 0.96  _(volume normal)_
- **Choppiness** : 52.6  _(transition)_
- **MA** : MA20 61.96 · MA50 53.62 · MA200 49.45  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 +7.9% · MA200 +17.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (27428 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
