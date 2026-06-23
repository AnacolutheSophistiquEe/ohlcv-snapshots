# MSTR

**Generated** : 2026-06-23T00:12:31.648366+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $109.46  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $109.46 (+10.8% vs entrée) · entrée $98.78 · stop $95.58 · T1 $101.42 · R/R 0.82  
> ↳ P(T1 av. stop) 45 % · EV/risk -0.032 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $98.25–$99.31 (mid $98.78)
- Spot actuel : $109.46 (+10.8% au-dessus de la zone — repli à attendre)
- Stop : $95.58 (stop swing-based (1.53%))
- Targets : T1 $101.42 · R/R 0.82 | T2 $104.06 · R/R 1.65 | T3 $106.70 · R/R 2.47
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $95.58


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : $-0.101 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 45 % | T2 20 % | T3 8 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 25.1 | bear 69.4 | side 5.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 185 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (trop peu de remplissages (4))
  - **swing** : indisponible (trop peu de remplissages (1))
  - **deep** : indisponible (trop peu de remplissages (0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→69% · +2.0%→50% · +3.0%→34% · +5.0%→12% · +8.0%→5%
- Range intraday médian 5.33% (p90 8.98%) · excursion haute méd. +2.01% / basse méd. −2.84%
- Profil de vol intra : ouverture 2.986% vs midi 1.295% vs clôture 1.277% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.62 · part idiosyncratique 0.17
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 27.9  _(survente)_
- **ADX** : 26.6  _(tendance etablie)_
- **MACD** : hist -1.286  _(pas de croisement recent)_
- **BB** : %B 0.17 · largeur 52.0%
- **ATR** : 10.68 (34.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.232  _(distribution)_
- **Vol ratio** : 1.13  _(volume normal)_
- **Choppiness** : 54.5  _(transition)_
- **MA** : MA20 132.16 · MA50 154.07 · MA200 190.73  _(prix < MA20)_
- **Dist MA** : MA20 -17.2% · MA50 -29.0% · MA200 -42.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (21556 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
