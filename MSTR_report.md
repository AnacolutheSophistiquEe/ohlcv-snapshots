# MSTR

**Generated** : 2026-06-23T21:47:26.142261+00:00  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $103.84  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $103.84 (+10.6% vs entrée) · entrée $93.86 · stop $90.86 · T1 $96.39 · R/R 0.84  
> ↳ P(T1 av. stop) 37 % · EV/risk -0.041 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -162 % hors [0,100] (R² max 0.04). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $93.35–$94.36 (mid $93.86)
- Spot actuel : $103.84 (+10.6% au-dessus de la zone — repli à attendre)
- Stop : $90.86 (stop swing_plan-based (-22.11%))
- Targets : T1 $96.39 · R/R 0.84 | T2 $98.92 · R/R 1.69 | T3 $101.46 · R/R 2.53
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $90.86


## Edge, scénarios & sizing

- EV/risk : -0.041 | EV/share : $-0.122 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 11 % | T3 2 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 7.7 | bear 81.5 | side 10.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→82% · +1.0%→70% · +2.0%→52% · +3.0%→31% · +5.0%→9% · +8.0%→4%
- Range intraday médian 5.12% (p90 8.46%) · excursion haute méd. +2.24% / basse méd. −2.89%
- Profil de vol intra : ouverture 3.011% vs midi 1.188% vs clôture 1.217% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.013)_ ; drift intra méd. -1.176% ; recovery-V 32%
- **σ réalisé intraday** 3.723% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 72% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 110.3259 (VA 107.5066–113.4584 ; dernier close 109.53)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.6 · part idiosyncratique 0.4
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.6  _(momentum baissier)_
- **ADX** : 27.3  _(tendance etablie)_
- **MACD** : hist -1.523  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 52.6%
- **ATR** : 9.98 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.249  _(distribution)_
- **Vol ratio** : 1.03  _(volume normal)_
- **Choppiness** : 52.8  _(transition)_
- **MA** : MA20 129.36 · MA50 153.58 · MA200 189.62  _(prix < MA20)_
- **Dist MA** : MA20 -19.7% · MA50 -32.4% · MA200 -45.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (24015 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
