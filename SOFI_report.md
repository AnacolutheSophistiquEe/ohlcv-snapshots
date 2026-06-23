# SOFI

**Generated** : 2026-06-23T21:59:32.443957+00:00  
**Santé technique** : 5/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $17.29  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $17.29 (+5.2% vs entrée) · entrée $16.44 · stop $16.04 · T1 $17.23 · R/R 1.97  
> ↳ P(T1 av. stop) 34 % · EV/risk 0.009 · ¼-Kelly 0.001 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

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

Plan privilegie B (swing), composite 5/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $16.28–$16.60 (mid $16.44)
- Spot actuel : $17.29 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $16.04 (stop swing_plan-based (-7.21%))
- Targets : T1 $17.23 · R/R 1.97 | T2 $18.02 · R/R 3.95 | T3 $18.81 · R/R 5.92
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $16.04


## Edge, scénarios & sizing

- EV/risk : 0.009 | EV/share : $0.003 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.004 | ¼-Kelly 0.001 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, swing) : bull 23.2 | bear 43.4 | side 33.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 277.0 (= 16 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.243% → cible +2.154% / stop −1.756%, p_fill 54%, n_eff≈19.0) : P(cible|rempli) **27%** · **EV/risk +0.042** (×p_fill ; si rempli +0.14% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=15, n_eff=7))
  - **deep** (entrée dip −7.614% → cible +6.812% / stop −3.406%, p_fill 22%, n_eff≈8.2) : P(cible|rempli) **27%** · **EV/risk -0.054** (×p_fill ; si rempli -0.83% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→71% · +2.0%→46% · +3.0%→35% · +5.0%→8% · +8.0%→0%
- Range intraday médian 4.38% (p90 6.64%) · excursion haute méd. +1.89% / basse méd. −2.16%
- Profil de vol intra : ouverture 2.942% vs midi 0.942% vs clôture 1.022% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.113 ; momentum — autocorr 0.038)_ ; drift intra méd. -0.079% ; recovery-V 36%
- **σ réalisé intraday** 3.102% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 59% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 17.2782 (VA 17.1803–17.3272 ; dernier close 17.09)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.38 · part idiosyncratique 0.62
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 47.0  _(neutre)_
- **ADX** : 19.6  _(pas de tendance nette)_
- **MACD** : hist 0.083  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 17.9%
- **ATR** : 0.99 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.055  _(distribution)_
- **Vol ratio** : 1.06  _(volume normal)_
- **Choppiness** : 57.4  _(transition)_
- **MA** : MA20 17.01 · MA50 16.98 · MA200 22.62  _(prix > MA20)_
- **Dist MA** : MA20 +1.7% · MA50 +1.8% · MA200 -23.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (29726 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
