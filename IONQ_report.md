# IONQ

**Generated** : 2026-06-23T00:16:43.414629+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $58.32  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $58.32 (+4.2% vs entrée) · entrée $55.97 · stop $54.24 · T1 $57.89 · R/R 1.11  
> ↳ P(T1 av. stop) 44 % · EV/risk 0.035 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $55.59–$56.36 (mid $55.97)
- Spot actuel : $58.32 (+4.2% au-dessus de la zone — repli à attendre)
- Stop : $54.24 (stop swing-based (-10.65%))
- Targets : T1 $57.89 · R/R 1.11 | T2 $59.81 · R/R 2.22 | T3 $61.73 · R/R 3.33
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $54.24


## Edge, scénarios & sizing

- EV/risk : 0.035 | EV/share : $0.060 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 21 % | T3 8 %
- Kelly (position) : f* 0.002 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 15.0 | bear 57.6 | side 27.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 233.0 (= 4 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 164 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.022% → cible +3.426% / stop −3.103%, p_fill 43%, 70 remplis) : P(cible|rempli) **30%** · **EV/risk -0.022** (×p_fill ; si rempli -0.16% du capital)
  - **swing** (entrée dip −8.848% → cible +7.661% / stop −3.831%, p_fill 23%, 37 remplis) : P(cible|rempli) **32%** · **EV/risk -0.006** (×p_fill ; si rempli -0.11% du capital)
  - **deep** (entrée dip −13.684% → cible +10.834% / stop −5.417%, p_fill 17%, 26 remplis) : P(cible|rempli) **31%** · **EV/risk -0.011** (×p_fill ; si rempli -0.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→80% · +2.0%→64% · +3.0%→49% · +5.0%→26% · +8.0%→12%
- Range intraday médian 7.45% (p90 12.73%) · excursion haute méd. +2.93% / basse méd. −3.4%
- Profil de vol intra : ouverture 4.418% vs midi 1.548% vs clôture 1.617% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.32
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.5  _(momentum baissier)_
- **ADX** : 23.0  _(pas de tendance nette)_
- **MACD** : hist -1.36  _(pas de croisement recent)_
- **BB** : %B 0.33 · largeur 36.9%
- **ATR** : 5.79 (87.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.027  _(neutre)_
- **Vol ratio** : 0.87  _(volume normal)_
- **Choppiness** : 51.7  _(transition)_
- **MA** : MA20 62.25 · MA50 53.03 · MA200 49.37  _(prix < MA20)_
- **Dist MA** : MA20 -6.3% · MA50 +10.0% · MA200 +18.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (25361 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
