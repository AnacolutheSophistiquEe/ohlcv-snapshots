# CEG

**Generated** : 2026-06-23T00:19:31.423975+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $275.53  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $275.53 (+3.7% vs entrée) · entrée $265.72 · stop $262.78 · T1 $270.13 · R/R 1.5  
> ↳ P(T1 av. stop) 41 % · EV/risk 0.075 · ¼-Kelly 0.005 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $264.84–$266.61 (mid $265.72)
- Spot actuel : $275.53 (+3.7% au-dessus de la zone — repli à attendre)
- Stop : $262.78 (stop atr-based (-5.34%))
- Targets : T1 $270.13 · R/R 1.5 | T2 $274.54 · R/R 3.0 | T3 $278.95 · R/R 4.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $262.78


## Edge, scénarios & sizing

- EV/risk : 0.075 | EV/share : $0.220 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 41 % | T2 20 % | T3 8 %
- Kelly (position) : f* 0.02 | ¼-Kelly 0.005 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 60.6 | bear 19.9 | side 19.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 160 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.562% → cible +1.659% / stop −1.107%, p_fill 19%, 31 remplis) : P(cible|rempli) **23%** · **EV/risk -0.050** (×p_fill ; si rempli -0.29% du capital)
  - **swing** (entrée dip −7.117% → cible +3.71% / stop −1.855%, p_fill 10%, 16 remplis) : P(cible|rempli) **19%** · **EV/risk -0.031** (×p_fill ; si rempli -0.56% du capital)
  - **deep** (entrée dip −10.676% → cible +5.247% / stop −2.624%, p_fill 10%, 15 remplis) : P(cible|rempli) **33%** · **EV/risk -0.003** (×p_fill ; si rempli -0.07% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→66% · +2.0%→38% · +3.0%→28% · +5.0%→8% · +8.0%→0%
- Range intraday médian 3.72% (p90 7.02%) · excursion haute méd. +1.6% / basse méd. −1.61%
- Profil de vol intra : ouverture 2.635% vs midi 0.736% vs clôture 0.775% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.32 · part idiosyncratique 9.7
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.6  _(momentum haussier)_
- **ADX** : 19.3  _(pas de tendance nette)_
- **MACD** : hist 2.793  _(bullish_recent)_
- **BB** : %B 0.6 · largeur 24.5%
- **ATR** : 9.81 (4.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF -0.159  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 44.6  _(transition)_
- **MA** : MA20 268.78 · MA50 284.12 · MA200 318.28  _(prix > MA20)_
- **Dist MA** : MA20 +2.5% · MA50 -3.0% · MA200 -13.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (24149 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
