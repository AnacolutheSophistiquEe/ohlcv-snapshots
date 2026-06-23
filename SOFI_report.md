# SOFI

**Generated** : 2026-06-23T00:23:31.321507+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.10  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $17.10 (+4.6% vs entrée) · entrée $16.35 · stop $15.96 · T1 $17.14 · R/R 2.03  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.009 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.070 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.20–$16.51 (mid $16.35)
- Spot actuel : $17.10 (+4.6% au-dessus de la zone — repli à attendre)
- Stop : $15.96 (stop atr-based (-8.79%))
- Targets : T1 $17.14 · R/R 2.03 | T2 $17.93 · R/R 4.05 | T3 $18.72 · R/R 6.08
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.96


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 33.2 | bear 20.6 | side 46.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 154.0 (= 9 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 161 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s ; entrée au DIP du plan + p_fill ; à comparer à l'EV GBM du bloc Edge — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.983% → cible +2.154% / stop −1.792%, p_fill 49%, 79 remplis) : P(cible|rempli) **29%** · **EV/risk -0.018** (×p_fill ; si rempli -0.07% du capital)
  - **swing** (entrée dip −4.367% → cible +4.817% / stop −2.408%, p_fill 32%, 51 remplis) : P(cible|rempli) **31%** · **EV/risk -0.046** (×p_fill ; si rempli -0.34% du capital)
  - **deep** (entrée dip −6.754% → cible +6.813% / stop −3.406%, p_fill 35%, 53 remplis) : P(cible|rempli) **23%** · **EV/risk -0.137** (×p_fill ; si rempli -1.34% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→68% · +2.0%→44% · +3.0%→31% · +5.0%→8% · +8.0%→0%
- Range intraday médian 4.27% (p90 7.7%) · excursion haute méd. +1.88% / basse méd. −1.95%
- Profil de vol intra : ouverture 2.827% vs midi 0.935% vs clôture 1.056% _(ouverture ~3.0× plus volatile → privilégier/éviter selon le setup)_


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.4 · part idiosyncratique 0.14
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.0  _(momentum baissier)_
- **ADX** : 19.6  _(pas de tendance nette)_
- **MACD** : hist 0.101  _(pas de croisement recent)_
- **BB** : %B 0.55 · largeur 19.4%
- **ATR** : 1.0 (32.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.068  _(distribution)_
- **Vol ratio** : 0.9  _(volume normal)_
- **Choppiness** : 57.8  _(transition)_
- **MA** : MA20 16.92 · MA50 16.96 · MA200 22.66  _(prix > MA20)_
- **Dist MA** : MA20 +1.0% · MA50 +0.8% · MA200 -24.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (27895 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
