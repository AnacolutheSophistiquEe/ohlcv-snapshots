# SMCI

**Generated** : 2026-06-23T00:13:56.393856+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 10.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite extreme · $35.46  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $35.46 (+13.7% vs entrée) · entrée $31.19 · stop $29.91 · T1 $32.99 · R/R 1.41  
> ↳ P(T1 av. stop) 40 % · EV/risk 0.057 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : divergent_short_long (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $30.83–$31.55 (mid $31.19)
- Spot actuel : $35.46 (+13.7% au-dessus de la zone — repli à attendre)
- Stop : $29.91 (stop atr-based (-18.05%))
- Targets : T1 $32.99 · R/R 1.41 | T2 $34.79 · R/R 2.81 | T3 $36.59 · R/R 4.22
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $29.91


## Edge, scénarios & sizing

- EV/risk : 0.057 | EV/share : $0.073 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 19 % | T3 8 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 32.7 | bear 54.1 | side 13.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 165 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (trop peu de remplissages (2))
  - **swing** : indisponible (trop peu de remplissages (2))
  - **deep** : indisponible (trop peu de remplissages (2))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→69% · +2.0%→49% · +3.0%→35% · +5.0%→19% · +8.0%→8%
- Range intraday médian 5.12% (p90 9.51%) · excursion haute méd. +1.9% / basse méd. −2.43%
- Profil de vol intra : ouverture 3.23% vs midi 1.113% vs clôture 1.242% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.45 · part idiosyncratique 0.17
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.1  _(momentum baissier)_
- **ADX** : 28.6  _(tendance etablie)_
- **MACD** : hist -1.304  _(pas de croisement recent)_
- **BB** : %B 0.41 · largeur 76.1%
- **ATR** : 4.27 (97.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.027  _(neutre)_
- **Vol ratio** : 1.66  _(volume au-dessus de la moyenne)_
- **Choppiness** : 35.0  _(marche directionnel)_
- **MA** : MA20 38.08 · MA50 33.05 · MA200 35.53  _(prix < MA20)_
- **Dist MA** : MA20 -6.9% · MA50 +7.3% · MA200 -0.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (21316 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
