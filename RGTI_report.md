# RGTI

**Generated** : 2026-06-23T21:53:34.977211+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $21.28  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $21.28 (+2.1% vs entrée) · entrée $20.84 · stop $20.10 · T1 $21.61 · R/R 1.04  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.131 _(réel 5 s)_ (GBM -0.006) · ¼-Kelly 0.0 · _probas brutes (Monte-Carlo), non calibrées · n=0_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.040 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $20.68–$20.99 (mid $20.84)
- Spot actuel : $21.28 (+2.1% au-dessus de la zone — repli à attendre)
- Stop : $20.10 (stop swing_plan-based (-8.51%))
- Targets : T1 $21.61 · R/R 1.04 | T2 $22.38 · R/R 2.08 | T3 $23.15 · R/R 3.12
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $20.10


## Edge, scénarios & sizing

- EV/risk : -0.006 | EV/share : $-0.004 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ EV négatif ⇒ Pass)_
- Calibration des probas : _probas brutes (Monte-Carlo), non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 26.1 | bear 65.0 | side 8.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 149.0 (= 7 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.072% → cible +3.694% / stop −3.531%, p_fill 64%, n_eff≈25.2) : P(cible|rempli) **35%** · **EV/risk -0.131** (×p_fill ; si rempli -0.72% du capital)
  - **swing** (entrée dip −4.568% → cible +8.261% / stop −4.13%, p_fill 58%, n_eff≈23.5) : P(cible|rempli) **25%** · **EV/risk -0.187** (×p_fill ; si rempli -1.32% du capital)
  - **deep** (entrée dip −7.05% → cible +11.683% / stop −5.842%, p_fill 59%, n_eff≈20.0) : P(cible|rempli) **27%** · **EV/risk -0.095** (×p_fill ; si rempli -0.95% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→82% · +2.0%→68% · +3.0%→52% · +5.0%→36% · +8.0%→15%
- Range intraday médian 8.01% (p90 13.36%) · excursion haute méd. +3.31% / basse méd. −3.11%
- Profil de vol intra : ouverture 4.886% vs midi 1.702% vs clôture 2.016% _(ouverture ~2.9× plus volatile → privilégier/éviter selon le setup)_
- **Régime intraday** : **chop** _(efficiency 0.128 ; momentum — autocorr 0.053)_ ; drift intra méd. 0.81% ; recovery-V 52%
- **σ réalisé intraday** 5.743% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 62% / bas 43% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 21.9843 (VA 21.3197–22.0866 ; dernier close 21.38)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.51 · part idiosyncratique 0.49
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-06-25 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 33.2  _(momentum baissier)_
- **ADX** : 18.1  _(pas de tendance nette)_
- **MACD** : hist -0.305  _(pas de croisement recent)_
- **BB** : %B 0.36 · largeur 43.2%
- **ATR** : 2.45 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.043  _(neutre)_
- **Vol ratio** : 0.89  _(volume normal)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 22.69 · MA50 20.09 · MA200 23.81  _(prix < MA20)_
- **Dist MA** : MA20 -6.2% · MA50 +5.9% · MA200 -10.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (29885 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
