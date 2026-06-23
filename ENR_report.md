# ENR

**Generated** : 2026-06-23T00:05:58.017457+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €169.64  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €169.64 (+1.6% vs entrée) · entrée €167.02 · stop €163.56 · T1 €173.93 · R/R 2.0  
> ↳ P(T1 av. stop) 37 % · EV/risk 0.128 · ¼-Kelly 0.008 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.110 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : €165.64–€168.40 (mid €167.02)
- Spot actuel : €169.64 (+1.6% au-dessus de la zone — repli à attendre)
- Stop : €163.56 (stop sr-based (-3.24%))
- Targets : T1 €173.93 · R/R 2.0 | T2 €180.85 · R/R 4.0 | T3 €187.76 · R/R 5.99
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €163.56


## Edge, scénarios & sizing

- EV/risk : 0.128 | EV/share : €0.443 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 20 % | T3 9 %
- Kelly (position) : f* 0.032 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 48.0 | bear 31.3 | side 20.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 509.0 (= 3 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 164 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.705% → cible +1.851% / stop −1.315%, p_fill 77%, 126 remplis) : P(cible|rempli) **25%** · **EV/risk -0.117** (×p_fill ; si rempli -0.20% du capital)
  - **swing** (entrée dip −1.542% → cible +4.14% / stop −2.07%, p_fill 69%, 111 remplis) : P(cible|rempli) **33%** · **EV/risk -0.016** (×p_fill ; si rempli -0.05% du capital)
  - **deep** (entrée dip −2.383% → cible +5.854% / stop −2.927%, p_fill 66%, 102 remplis) : P(cible|rempli) **36%** · **EV/risk +0.094** (×p_fill ; si rempli +0.42% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→40% · +3.0%→23% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.87% (p90 6.68%) · excursion haute méd. +1.5% / basse méd. −1.6%
- Profil de vol intra : ouverture 2.057% vs midi 0.938% vs clôture 1.231% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.58 · part idiosyncratique 0.29
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 60.1  _(momentum haussier)_
- **ADX** : 20.4  _(pas de tendance nette)_
- **MACD** : hist 2.152  _(bullish_recent)_
- **BB** : %B 0.73 · largeur 24.4%
- **ATR** : 7.38 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.108  _(distribution)_
- **Vol ratio** : 0.45  _(volume atone)_
- **Choppiness** : 40.5  _(transition)_
- **MA** : MA20 160.45 · MA50 169.26 · MA200 136.4  _(prix > MA20)_
- **Dist MA** : MA20 +5.7% · MA50 +0.2% · MA200 +24.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (26702 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
