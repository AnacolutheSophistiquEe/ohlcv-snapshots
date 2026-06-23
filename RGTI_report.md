# RGTI

**Generated** : 2026-06-23T00:18:08.902192+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 8.0 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $21.38  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $21.38 (+5.5% vs entrée) · entrée $20.27 · stop $19.55 · T1 $21.16 · R/R 1.24  
> ↳ P(T1 av. stop) 42 % · EV/risk 0.027 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $20.09–$20.45 (mid $20.27)
- Spot actuel : $21.38 (+5.5% au-dessus de la zone — repli à attendre)
- Stop : $19.55 (stop swing-based (-15.87%))
- Targets : T1 $21.16 · R/R 1.24 | T2 $22.05 · R/R 2.47 | T3 $22.94 · R/R 3.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $19.55


## Edge, scénarios & sizing

- EV/risk : 0.027 | EV/share : $0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 42 % | T2 20 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 28.5 | bear 58.6 | side 12.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 150.0 (= 7 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 160 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −5.18% → cible +4.383% / stop −3.575%, p_fill 32%, 52 remplis) : P(cible|rempli) **21%** · **EV/risk -0.025** (×p_fill ; si rempli -0.27% du capital)
  - **swing** (entrée dip −11.398% → cible +9.8% / stop −4.9%, p_fill 15%, 23 remplis) : P(cible|rempli) **35%** · **EV/risk +0.029** (×p_fill ; si rempli +0.95% du capital)
  - **deep** (entrée dip −17.622% → cible +13.859% / stop −6.93%, p_fill 11%, 17 remplis) : P(cible|rempli) **41%** · **EV/risk +0.022** (×p_fill ; si rempli +1.35% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→79% · +2.0%→63% · +3.0%→52% · +5.0%→32% · +8.0%→12%
- Range intraday médian 7.72% (p90 13.03%) · excursion haute méd. +3.15% / basse méd. −3.39%
- Profil de vol intra : ouverture 4.606% vs midi 1.646% vs clôture 1.92% _(ouverture ~2.8× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.44
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 38.1  _(momentum baissier)_
- **ADX** : 19.4  _(pas de tendance nette)_
- **MACD** : hist -0.355  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 44.6%
- **ATR** : 2.42 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF 0.047  _(neutre)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 47.8  _(transition)_
- **MA** : MA20 22.95 · MA50 19.96 · MA200 23.78  _(prix < MA20)_
- **Dist MA** : MA20 -6.8% · MA50 +7.1% · MA200 -10.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (25964 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
