# EVT

**Generated** : 2026-06-23T21:38:46.569989+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · €4.70  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €4.70 (+1.5% vs entrée) · entrée €4.63 · stop €4.58 · T1 €4.70 · R/R 1.4  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.037 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -124 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €4.62–€4.65 (mid €4.63)
- Spot actuel : €4.70 (+1.5% au-dessus de la zone — repli à attendre)
- Stop : €4.58 (stop swing_plan-based (-4.71%))
- Targets : T1 €4.70 · R/R 1.4 | T2 €4.77 · R/R 2.8 | T3 €4.83 · R/R 4.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €4.58


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : €-0.001 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 23 % | T3 11 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 11.2 | bear 6.2 | side 82.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.431% → cible +1.431% / stop −1.146%, p_fill 67%, n_eff≈27.6) : P(cible|rempli) **40%** · **EV/risk -0.037** (×p_fill ; si rempli -0.06% du capital)
  - **swing** (entrée dip −3.162% → cible +3.2% / stop −1.599%, p_fill 48%, n_eff≈18.3) : P(cible|rempli) **25%** · **EV/risk -0.149** (×p_fill ; si rempli -0.50% du capital)
  - **deep** (entrée dip −4.88% → cible +4.523% / stop −2.26%, p_fill 53%, n_eff≈18.2) : P(cible|rempli) **20%** · **EV/risk -0.241** (×p_fill ; si rempli -1.03% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→66% · +2.0%→41% · +3.0%→25% · +5.0%→8% · +8.0%→2%
- Range intraday médian 4.77% (p90 7.61%) · excursion haute méd. +1.75% / basse méd. −2.44%
- Profil de vol intra : ouverture 2.973% vs midi 1.271% vs clôture 1.286% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.096 ; mean-reverting — autocorr -0.13)_ ; drift intra méd. -0.228% ; recovery-V 41%
- **σ réalisé intraday** 3.056% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 71% / whipsaw 41%
- POC intraday (dernière séance, temps-au-prix) : 4.6504 (VA 4.6055–4.6607 ; dernier close 4.636)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.17 · part idiosyncratique 0.83
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.1  _(momentum baissier)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist -0.016  _(pas de croisement recent)_
- **BB** : %B 0.32 · largeur 18.8%
- **ATR** : 0.18 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.163  _(accumulation)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 49.1  _(transition)_
- **MA** : MA20 4.87 · MA50 5.06 · MA200 5.58  _(prix < MA20)_
- **Dist MA** : MA20 -3.4% · MA50 -7.2% · MA200 -15.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (25301 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
