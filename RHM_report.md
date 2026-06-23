# RHM

**Generated** : 2026-06-23T00:02:01.797583+00:00  
**Santé technique** : 3/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : range · volatilite low · €1181.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €1181.40 (+1.1% vs entrée) · entrée €1168.28 · stop €1153.34 · T1 €1183.79 · R/R 1.04  
> ↳ P(T1 av. stop) 43 % · EV/risk -0.054 · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.060 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €1165.17–€1171.38 (mid €1168.28)
- Spot actuel : €1181.40 (+1.1% au-dessus de la zone — repli à attendre)
- Stop : €1153.34 (stop sr-based (-4.87%))
- Targets : T1 €1183.79 · R/R 1.04 | T2 €1199.30 · R/R 2.08 | T3 €1214.81 · R/R 3.11
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €1153.34


## Edge, scénarios & sizing

- EV/risk : -0.054 | EV/share : €-0.814 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 19 % | T3 7 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 29.5 | bear 31.7 | side 38.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 181 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.106% → cible +1.328% / stop −1.278%, p_fill 65%, 118 remplis) : P(cible|rempli) **42%** · **EV/risk -0.022** (×p_fill ; si rempli -0.04% du capital)
  - **swing** (entrée dip −2.442% → cible +2.969% / stop −1.484%, p_fill 47%, 84 remplis) : P(cible|rempli) **25%** · **EV/risk -0.143** (×p_fill ; si rempli -0.45% du capital)
  - **deep** (entrée dip −3.78% → cible +4.199% / stop −2.099%, p_fill 51%, 88 remplis) : P(cible|rempli) **25%** · **EV/risk -0.149** (×p_fill ; si rempli -0.61% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→60% · +2.0%→36% · +3.0%→22% · +5.0%→3% · +8.0%→0%
- Range intraday médian 3.44% (p90 6.34%) · excursion haute méd. +1.53% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.268% vs midi 0.844% vs clôture 0.932% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.33 · part idiosyncratique 0.26
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.2  _(neutre)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist 4.134  _(pas de croisement recent)_
- **BB** : %B 0.34 · largeur 12.2%
- **ATR** : 49.77 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.06  _(distribution)_
- **Vol ratio** : 0.57  _(volume atone)_
- **Choppiness** : 71.1  _(marche en range (choppy))_
- **MA** : MA20 1205.16 · MA50 1271.88 · MA200 1581.39  _(prix < MA20)_
- **Dist MA** : MA20 -2.0% · MA50 -7.1% · MA200 -25.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (23880 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
